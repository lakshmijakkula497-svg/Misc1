Total Agreements =
DISTINCTCOUNTNOBLANK(
    dim_commercial_agreement_base[CAC_Agreement_Id]
)


Average Loss Paid per Claim =
DIVIDE(
    [Total Loss Paid],
    [Total Claims],
    0
)


Average Payment per Claim =
DIVIDE(
    [Total Payment Amount],
    [Total Claims],
    0
)


Average Loss Paid per Feature =
DIVIDE(
    [Total Loss Paid],
    [Total Claim Features],
    0
)


Average Features per Claim =
DIVIDE(
    [Total Claim Features],
    [Total Claims],
    0
)


Total Payment Transactions =
DISTINCTCOUNTNOBLANK(
    fact_claim_feature_payment_log[Claim_Feature_Payment_Log_Id]
)


Total Reserve Transactions =
DISTINCTCOUNTNOBLANK(
    fact_claim_feature_reserve_log[Claim_Feature_Reserve_Log_Id]
)


Total Claimants =
DISTINCTCOUNTNOBLANK(
    dim_claim_feature_base[Claimant_Id]
)
