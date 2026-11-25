SELECT
    Claim_Folder_Id,
    COUNT(*) AS total_records,
    SUM(
        CASE
            WHEN CAST(Valid_To_Date AS DATE) = DATE '9999-12-31'
            THEN 1
            ELSE 0
        END
    ) AS current_records
FROM edl.edw_dbo.dim_claim_folder_base
GROUP BY Claim_Folder_Id
HAVING current_records <> 1
ORDER BY current_records DESC;
