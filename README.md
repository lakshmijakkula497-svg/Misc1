Category =
SWITCH(
    TRUE(),
    'Ad Hoc Fields'[Ad Hoc Fields Order] <= 2, "Calendar",
    'Ad Hoc Fields'[Ad Hoc Fields Order] <= 13, "Metrics",
    "Fields"
)
