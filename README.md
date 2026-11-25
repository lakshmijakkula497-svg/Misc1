In the EDW table "edl.edw_dbo.dim_commercial_agreement_base", after applying the SCD Type 2 filter "Current_Row_Indicator = 'Y'", I identified 42,250,459 current records with unique "CAC_Agreement_Version_Id" values. However, 5,945,705 records (14.07%) have "Insured_Id = '-1'", and none have NULL Insured IDs.

Could you clarify the following based on existing EDW documentation, source-to-target mappings, ETL logic, Jira tickets and established reporting practices?

1. What does "Insured_Id = '-1'" represent in this table?
2. Is this expected business behavior, a default warehouse value, a source-system limitation, or a known data quality issue?
3. Are there specific source systems where this behavior is expected?
4. Is there an alternative table or mapping to retrieve the correct Insured ID for these records?
5. What is the recommended join condition between the commercial agreement dimension and the insured dimension?
6. For claims reporting, should we use the current SCD Type 2 record or the historical record corresponding to the claim's date of loss?
7. How should records with "Insured_Id = '-1'" be handled in the Power BI claims semantic model without losing claims or duplicating financial measures?

Please provide references to relevant internal documentation, Jira tickets, existing reporting implementations and recommended SQL join and filtering logic. Distinguish documented business rules from assumptions.
