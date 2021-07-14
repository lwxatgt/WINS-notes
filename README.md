# FROM FIN TO APPLICATION TO UEN DIV BRANCH

From FIN we go to 
1. TESTOS.Applicant, match via `FIN`

From there we get the `ID` which is the same as `APPLICATIONID` in `COY` Table

2. We take the `ID` and go to TESTOS.COY, 
querying

```sql
WHERE APPLICATIONID = ID
```

3. And we take the `COMPANYCODE` which is the same as the `LEGACYID` in company table

4. We then lookup the company table for the `DIVISION` and `BRANCH` info. Probably any info about company is taken from here but not confirmed.
