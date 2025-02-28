java c
DAT 560G: Database Design and SQL
Spring 2025, Mini A
Assignment #2: SQL Part 1
Instructions
1. This is an individual assignment. You may not discuss your approach to solving these questions with anyone, other than the instructor or TA.
2. Please include only your Student ID on the submission.
3. The only allowed material is:
            a. Class notes
            b. Content posted on Canvas
            c. Textbook
4. You are not permitted to use other online resources
5. Questions 1 – 6 are auto-graded on Canvas due by 6 am the day of the next lab
6. The other questions are due on Canvas, by the next lab
7. There will be TA office hours. See the schedule on Canvas.
Background
Renting an apartment with roommates is guaranteed to be a new experience. You’ll make memories with your roommates, learn about their culture and hobbies, and learn how you cope with others in different times.
The database here is focused on renting out apartments to people with roommates. The people renting the apartments are one part of the database, but not the important part of it. We are mostly interested in the apartment buildings, and the owners of apartment buildings.
An apartment building has information about the date built and the year built. We also maintain information on address, city, and number of apartments in the building. Each apartment may be rented to one, or more, people. Other information we have is the total monthly rent for all tenants and the value of the apartment building, if it were sold. A property manager runs the individual apartment buildings. We also have the gender of the property manager.
Buildings (Building, DateBuilt, YearBuilt, Address, City, Apartments, TotalRent, Value, PropertyManager, Gender)
The apartment building is owned by a single company, or be several companies. Each company may own one, or more, apartment buildings. They may also only partial ownership of an apartment building. In that case, they would be partners with other companies. The Property attribute in the Ownership relation is identical to the Building attribute in the Buildings relation. (It’s a foreign key.)   
For each owner we maintain information about what percent of the building that company owns. To give an example, if a building is owned by 3 companies, each with a different share, the ownership fraction for each company could be 33%, or one company may own a larger share. In another case, only 1 company owns the building. In this case, their ownership share would be 100%.
Information about the owners includes the city they are in, the number of partners, date the company was founded, and the number of times the partners meet each year. We also have information about the total assets owned by this company (in $M). The company has a manager. The manager’s gender is also kept.
Owners (Company, City, Partners, Meetings, DateFounded, Assets, Manager, Gender)
For each owner, in each building, we also know the date they purchased their share of the building. (To clarify, each company may have bought their share at a different time.) We also know what percent of their ownership stake has a mortgage on it. In the same building it could be that one owner has a mortgage of 80%, while another does not have a mortgage.
Ownership (Property, Company, Percent, PurchaseDate, PurchaseYear, Mortgage)
Tenant information in the database includes information about the people renting apartments. Each apartment may have one, or more, tenants. Frequently, roommates rent an apartment together. In addition to the tenants name, gender, and age, we have information about the apartment. This information includes the building name, the apartment number within the building, and the size of the apartment. Information about the lease includes the date this person started to rent the apartment, their monthly rent, and the duration of the代 写DAT 560G: Database Design and SQL Spring 2025 Assignment #2: SQL Part 1SQL
代做程序编程语言 lease in months.
Since many of the apartments have sublets, renters in the same apartment may have started their lease at different dates.
Tenants (Building, Tenant, Gender, Age, Apartment, Size, Rent, LeaseStart, Duration)
Database
The E/R Diagram for the database is below.

Relations:
Buildings (Building, DateBuilt, YearBuilt, Address, City, Apartments, TotalRent, Value, PropertyManager, Gender)
Owners (Company, City, Partners, Meetings, DateFounded, Assets, Manager, Gender)
Ownership (Property, Company, Percent, PurchaseDate, PurchaseYear, Mortgage)
Tenants (Building, Tenant, Gender, Age, Apartment, Size, Rent, LeaseStart, Duration)
Each of these questions is 10 points. Submit answers to these online on Canvas, by midnight the day before the lab. They are automatically graded.
1) For each building list the year it was built, total rent, city, and its property manager. Sort the results by descending order of the total rent.
2) Identify all buildings with more than 25 apartments in Chesterfield, or St. Louis. List the building, apartments, and city. List the result in increasing order of value.
3) For each building with male tenants, find the average age of tenants, and min, and max of their rent.
4) For each city in the owner table, find the average number of partners, average assets, and total number of companies that a female manages.
5) For each company in the ownership table that owns between (and includes) 60 to 100 percent of a single property, find its total mortgage, its latest purchase, and the number of mortgages it has. Sort the results in decreasing order of the number of Mortgages.
6) Identify Companies that purchased a property not in 2013 where the mortgage is more than 50. List the company, property, and percent. Order in percent.
Each of these questions is worth 5 points. Submit answers to these on Canvas at midnight the day before the lab. They will be graded by TAs.
For each question, submit your SQL code and a screenshot of the results. If the results are too long, partial results are fine. Include relevant attributes for each result, to explain that the result is correct. Do NOT include many unnecessary attributes. Do NOT use SELECT *.
7) For each City in the buildings table, find how many buildings are located in, the average total number of these buildings, the total value of these buildings, and the number of managers these buildings have. Sort the results in decreasing order of average TotalRent.
8) Find buildings with more than 5 tenants. List the building, number of tenants, and city. Sort by the number of tenants in decreasing order.
9) Looking at the buildings’ YearBuilt, find how many buildings are built each year. Include buildings in the city of University or buildings that were not built in 1950 and 2000 at all in the analysis. Sort the results by the number of buildings built each year.
10) For each Apartment of each building, find the number of different tenants that live in it. Rename this attribute. Sort the results by the name of the building, the number of tenants, using the name you gave this attribute.
11) Find buildings where it has more than 35 apartments or its owner has a percentage between 0 and 100. Include the information about the Percentage the company owns, the date the building was built, and the purchase date. Sort results by building.
12) Find companies managed by a female, and first purchased year of 2010. List the names of companies. List the name of the companies only once, and order by the name of the companies.
13) For each building find the number of its owners, the year built, the number of different years it was purchased, and the average mortgage. Also include the city of the building. Sort result by building.
14) How much time did you spend on this assignment?







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
