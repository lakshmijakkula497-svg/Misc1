SELECT
    COUNT(*) AS Total_Current_Rows,

    COUNT(DISTINCT CAC_Agreement_Version_Id)
        AS Unique_Version_IDs,

    COUNT(DISTINCT STRUCT(
        CAC_Agreement_Version_Id,
        CAC_Agreement_External_Source_Code_Id
    )) AS Unique_Composite_Keys,

    COUNT(*) -
    COUNT(DISTINCT CAC_Agreement_Version_Id)
        AS Duplicate_Version_Rows,

    COUNT(*) -
    COUNT(DISTINCT STRUCT(
        CAC_Agreement_Version_Id,
        CAC_Agreement_External_Source_Code_Id
    )) AS Duplicate_Composite_Rows,

    COUNT_IF(
        CAST(Valid_To_Date AS DATE) = DATE '9999-12-31'
    ) AS Open_Ended_Rows

FROM edl.edw_dbo.dim_commercial_agreement_base

WHERE Current_Row_Indicator = 'Y';
