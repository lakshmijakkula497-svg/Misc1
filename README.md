Total Claims =
DISTINCTCOUNT(
    dim_claim_folder_base[Claim_Folder_Id]
)


Total Claim Features =
DISTINCTCOUNT(
    dim_claim_feature_base[Claim_Feature_Claim_Id]
)


Total Loss Paid =
SUM(
    fact_claim_feature_payment_log[Loss_Paid_Amount]
)


Total Payment Amount =
SUM(
    fact_claim_feature_payment_log[Payment_Amount]
)
