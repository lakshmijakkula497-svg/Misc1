SELECT
    CAC_Agreement_Version_Id,
    COUNT(DISTINCT STRUCT(CAC_Agreement_Id))
        AS Agreement_IDs,
    COUNT(DISTINCT STRUCT(CAC_Agreement_External_Source_Code_Id))
        AS Source_Codes,
    COUNT(DISTINCT STRUCT(Commercial_Agreement_Name))
        AS Names,
    COUNT(DISTINCT STRUCT(Insured_Id))
        AS Insured_IDs,
    COUNT(DISTINCT STRUCT(Region_Id))
        AS Regions
FROM edl.edw_dbo.dim_commercial_agreement_base
GROUP BY CAC_Agreement_Version_Id
HAVING
    Agreement_IDs > 1
    OR Source_Codes > 1
    OR Names > 1
    OR Insured_IDs > 1
    OR Regions > 1
LIMIT 20;
