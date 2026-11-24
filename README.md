# Misc1

SELECT
    Effective_To_Date,
    COUNT(*) AS Record_Count
FROM 
GROUP BY Effective_To_Date
ORDER BY Record_Count DESC
LIMIT 20;
