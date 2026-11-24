# Misc1

WITH Distinct_Agreements AS (
    SELECT DISTINCT
        CAC_Agreement_Version_Id,
        CAC_Agreement_Id,
        CAC_Agreement_External_Source_Code_Id,
        Commercial_Agreement_Name,
        Insured_Id,
        Region_Id
    FROM edl.edw_dbo.dim_commercial_agreement_base
)
SELECT
    COUNT(*) AS Total_Rows,
    COUNT(DISTINCT CAC_Agreement_Version_Id) AS Unique_IDs,
    COUNT(*) - COUNT(DISTINCT CAC_Agreement_Version_Id)
        AS Duplicate_Rows
FROM Distinct_Agreements;
