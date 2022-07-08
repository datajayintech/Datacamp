# Self Join Practice
In this project I am taking on the role as a Data Analyst. 
The client would like to the percentage of population from 2010 to 2015
For each country code in the populations table.

# Step 1 

# Join the populations table to itself.

![image](https://user-images.githubusercontent.com/71678091/178048981-d547a547-5d99-4b4b-be36-b2d9afecc5f6.png)

# Results from Query 


![image](https://user-images.githubusercontent.com/71678091/178050625-b2101347-9852-4f58-bae1-f74f74dc653b.png)

Extend the ON in your query to include only those records where the 
p1.year (2010) matches with p2.year - 5 (2015 - 5 = 2010). 
This will omit the three entries per country_code that you aren't interested in.


![image](https://user-images.githubusercontent.com/71678091/178052291-049bd529-43bf-47ef-8ddc-f5395dec1880.png)


**SELECT** p1.country_code,p1.size AS size2010, p2. size AS size2015
		
		((p2.size - p1.size)/p1.size * 100.0) AS growth_perc 
		
**FROM** populations AS p1 <br>
 **INNER JOIN** pipulations AS p2 <br>
	  **ON** p1.country_code = p2.country_code <br>
		    **AND** p1.year = p2.year - 5; <br>
				
	**RESULTS** 
	![image](https://user-images.githubusercontent.com/71678091/178055949-74af54a8-ce2e-450d-a472-30b503ea5788.png)

	
				





