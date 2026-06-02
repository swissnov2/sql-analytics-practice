# sql-analytics-practice
SELECT 
    "CaseType",
    ROUND(AVG("DurationDays"), 1) AS average_days
FROM legal_cases
GROUP BY "CaseType"
HAVING AVG("DurationDays") > 400
ORDER BY average_days DESC;

SELECT "Country Name", "Country Code", "Series Name"
FROM population_latin_and_caribbean_countries
WHERE "Country Name" IN ('Brazil', 'Mexico', 'Colombia')
ORDER BY "Country Name" ASC;

SELECT "Country Name", "Country Code", "2019 [YR2019]" AS population_2019
FROM population_latin_and_caribbean_countries placc 
WHERE "Country Name" = 'Aruba'
      OR "Country Name" = 'Brazil'
ORDER BY "Country Name" ASC;

SELECT "Country Name", 
       "2019 [YR2019]" AS poulation_2019
FROM population_latin_and_caribbean_countries placc
WHERE "Country Name" LIKE 'C%'
      AND "2019 [YR2019]" IS NOT NULL
ORDER BY "2019 [YR2019]" ASC;

