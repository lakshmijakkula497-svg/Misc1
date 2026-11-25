SELECT
    CAC_Agreement_Version_Id,
    CAC_Agreement_Id,
    Insured_Id,
    Effective_From_Date,
    Effective_To_Date
FROM edl.edw_dbo.dim_commercial_agreement_base
WHERE CAC_Agreement_Version_Id IN (
    SELECT CAC_Agreement_Version_Id
    FROM edl.edw_dbo.dim_commercial_agreement_base
    GROUP BY CAC_Agreement_Version_Id
    HAVING COUNT(DISTINCT STRUCT(Insured_Id)) > 1
    LIMIT 5
)
ORDER BY
    CAC_Agreement_Version_Id,
    Effective_From_Date,
    Effective_To_Date;
