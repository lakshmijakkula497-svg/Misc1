WITH claims AS (
    SELECT DISTINCT Claim_Folder_Id
    FROM edl.edw_dbo.dim_claim_folder_base
    WHERE Current_Row_Indicator = 'Y'
      AND CAC_Agreement_Id = '0104037||20051021||74||53'
),
features AS (
    SELECT DISTINCT f.Claim_Feature_Claim_Id
    FROM edl.edw_dbo.dim_claim_feature_base f
    INNER JOIN claims c
        ON f.Claim_Folder_Claim_Id = c.Claim_Folder_Id
    WHERE f.Current_Row_Indicator = 'Y'
)
SELECT
    (SELECT COUNT(*) FROM claims) AS total_claims,
    (SELECT COUNT(*) FROM features) AS total_features,
    SUM(p.Loss_Paid_Amount) AS total_loss_paid,
    SUM(p.Payment_Amount) AS total_payment_amount
FROM edl.edw_dbo.fact_claim_feature_payment_log p
INNER JOIN features f
    ON p.Claim_Feature_Claim_Id = f.Claim_Feature_Claim_Id;
