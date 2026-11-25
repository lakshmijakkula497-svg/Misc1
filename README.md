dim_date =
VAR PaymentMin =
    MIN('fact_claim_feature_payment'[Transaction_Date])
VAR PaymentMax =
    MAX('fact_claim_feature_payment'[Transaction_Date])
VAR ReserveMin =
    MIN('fact_claim_feature_reserve'[Transaction_Date])
VAR ReserveMax =
    MAX('fact_claim_feature_reserve'[Transaction_Date])
VAR MinDate =
    MINX(
        FILTER(
            {PaymentMin, ReserveMin},
            NOT ISBLANK([Value])
        ),
        [Value]
    )
VAR MaxDate =
    MAX(PaymentMax, ReserveMax)
RETURN
    ADDCOLUMNS(
        CALENDAR(
            DATE(YEAR(MinDate), 1, 1),
            DATE(YEAR(MaxDate), 12, 31)
        ),
        "Year", YEAR([Date]),
        "Quarter", "Q" & QUARTER([Date]),
        "Month", FORMAT([Date], "MMMM"),
        "Month Short", FORMAT([Date], "MMM"),
        "Month Number", MONTH([Date]),
        "Year Month", FORMAT([Date], "MMM yyyy"),
        "Year Month Sort", YEAR([Date]) * 100 + MONTH([Date]),
        "Year Quarter", YEAR([Date]) & "-Q" & QUARTER([Date]),
        "Day", DAY([Date]),
        "Day Name", FORMAT([Date], "dddd"),
        "Day Number", WEEKDAY([Date], 2),
        "Week Number", WEEKNUM([Date], 2)
    )
