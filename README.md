SELECT
    COUNT(*) AS Total_Current_Rows,
    COUNT(DISTINCT Insured_Id) AS Unique_Insured_IDs,
    COUNT_IF(Insured_Id IS NULL) AS Null_Insured_IDs,
    COUNT_IF(Insured_Id = '-1') AS Unknown_Insured_IDs
FROM edl.edw_dbo.dim_commercial_agreement_base
WHERE Current_Row_Indicator = 'Y';
