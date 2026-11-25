Ad Hoc Fields = {
    ("Year", NAMEOF('dim_date'[Year]), 0),
    ("Quarter", NAMEOF('dim_date'[Quarter]), 1),
    ("Month", NAMEOF('dim_date'[Month]), 2),

    ("Average Features per Claim", NAMEOF('Metrics'[Average Features per Claim]), 3),
    ("Average Loss Paid per Feature", NAMEOF('Metrics'[Average Loss Paid per Feature]), 4),
    ("Average Payment per Claim", NAMEOF('Metrics'[Average Payment per Claim]), 5),
    ("Total Agreements", NAMEOF('Metrics'[Total Agreements]), 6),
    ("Total Claimants", NAMEOF('Metrics'[Total Claimants]), 7),
    ("Total Claim Features", NAMEOF('Metrics'[Total Claim Features]), 8),
    ("Total Claims", NAMEOF('Metrics'[Total Claims]), 9),
    ("Total Loss Paid", NAMEOF('Metrics'[Total Loss Paid]), 10),
    ("Total Payment Amount", NAMEOF('Metrics'[Total Payment Amount]), 11),
    ("Total Payment Transactions", NAMEOF('Metrics'[Total Payment Transactions]), 12),
    ("Total Reserve Transactions", NAMEOF('Metrics'[Total Reserve Transactions]), 13),

    ("CAC_Agreement_Id", NAMEOF('dim_commercial_agreement_base'[CAC_Agreement_Id]), 14),
    ("CAC_Agreement_Version_Id", NAMEOF('dim_commercial_agreement_base'[CAC_Agreement_Version_Id]), 15),
    ("Claim_Folder_Id", NAMEOF('dim_claim_folder_base'[Claim_Folder_Id]), 16),
    ("Claim_Folder_Number_Text", NAMEOF('dim_claim_folder_base'[Claim_Folder_Number_Text]), 17),
    ("Claim_Type_Id", NAMEOF('dim_claim_folder_base'[Claim_Type_Id]), 18),
    ("Claim_Feature_Claim_Id", NAMEOF('dim_claim_feature_base'[Claim_Feature_Claim_Id]), 19),
    ("Claim_Feature_Number_Text", NAMEOF('dim_claim_feature_base'[Claim_Feature_Number_Text]), 20),
    ("Claim_Exposure_Type_Id", NAMEOF('dim_claim_feature_base'[Claim_Exposure_Type_Id]), 21),
    ("Claimant_Id", NAMEOF('dim_claim_feature_base'[Claimant_Id]), 22)
}
