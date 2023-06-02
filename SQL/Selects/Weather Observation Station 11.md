Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.

Input Format

The STATION table is described as follows:



|  Field | Type |
|---|---|
| ID  | NUMBER |
| CITY | VARCHAR2(21)   |
| STATE  | VARCHAR2(2)  |
| LAT_N |  NUMBER |
| LONG_W | NUMBER |


**SOLUÇÃO**

SELECT DISTINCT CITY
FROM STATION
WHERE (CITY NOT LIKE 'a%'
AND CITY NOT LIKE 'e%'
AND CITY NOT LIKE 'i%'
AND CITY NOT LIKE 'o%'
AND CITY NOT LIKE 'u%')
OR (CITY NOT LIKE '%a'
AND CITY NOT LIKE '%e'
AND CITY NOT LIKE '%i'
AND CITY NOT LIKE '%o'
AND CITY NOT LIKE '%u')
