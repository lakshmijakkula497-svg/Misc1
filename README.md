# Misc1

SELECT
    CAC_Agreement_Version_Id,
    COUNT(*) AS Total_Records,
    COUNT(DISTINCT CAC_Agreement_Id) AS Agreement_IDs,
    COUNT(DISTINCT Commercial_Agreement_Name) AS Names,
    COUNT(DISTINCT Insured_Id) AS Insured_IDs,
    COUNT(DISTINCT Region_Id) AS Regions,
    COUNT(DISTINCT Effective_To_Date) AS End_Dates
FROM edl.edw_dbo.dim_commercial_agreement_base
GROUP BY CAC_Agreement_Version_Id
HAVING COUNT(*) > 1
ORDER BY Total_Records DESC
LIMIT 20;
