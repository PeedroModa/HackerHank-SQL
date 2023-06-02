Query the smallest Northern Latitude (LAT_N) from STATION that is greater than 38.7780 . Round your answer to  decimal places.

Input Format

The STATION table is described as follows:

| Field | Type |
|---|---|
| Id  | NUMBER |
| City | VARCHAR2 (21)   |
| State | VARCHAR2 (2)   |
| LAT_N | NUMBER  |
| LAT_W | NUMBER |

where LAT_N is the northern latitude and LONG_W is the western longitude.

**SOLUÇÃO**

```sql
SELECT ROUND(LAT_N,4)
FROM STATION
WHERE LAT_N = (SELECT MIN(LAT_N) FROM STATION WHERE LAT_N > 38.7780)
```
