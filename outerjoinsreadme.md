    --- In terms of life expectancy for 2010, determine the names of the lowest five countries and their regions
    
    --- Left Join
         SELECT c.name AS country, region, life_expectancy AS Life_exp
         FROM  countries AS C 
            LEFT JOIN populations AS p
              ON c.code = p.country_code
         WHERE year = 2010
            ORDER BY life_exp
            LIMIT 5; 
            readme.md
![image](https://user-images.githubusercontent.com/71678091/179375589-82aa8c4e-e170-4707-bcc9-820517872215.png)
