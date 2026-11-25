SELECT
    table_catalog,
    table_schema,
    table_name,
    column_name,
    data_type
FROM edl.information_schema.columns
WHERE LOWER(table_name) IN (
    'fact_claim_activity',
    'fact_claim_feature_daily_snapshot',
    'fact_claim_feature_monthly_snapshot',
    'dim_insured_base',
    'dim_insured'
)
AND LOWER(column_name) LIKE '%insured%'
ORDER BY table_schema, table_name, column_name;
