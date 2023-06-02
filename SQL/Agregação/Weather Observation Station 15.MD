Query the Western Longitude (LONG_W) for the largest Northern Latitude (LAT_N) in STATION that is less than 137.2345. Round your answer to  decimal places.

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
SELECT ROUND(LONG_W,4)
FROM STATION
WHERE LAT_N = (SELECT MAX(LAT_N) FROM STATION WHERE LAT_N < 137.2345)
```
