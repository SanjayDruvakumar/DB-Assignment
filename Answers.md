1st answer: "Product" and "Product_Category" entities establishes a one-to-many relationship between the two tables, where each product belongs to one category, 
and each category can have multiple products. 

Following steps shows the relationship of two entities:
The "Products" table includes a new column "Category_id" which serves as a foreign key referencing the primary key of the "Product_Category" table.
Each product in the "Products" table is associated with a specific category through the "Category_id".
The "Product_Category" table stores information about different categories, and each category has a unique ID.
The "Category-id" column in the "Products" table establishes the relationship between products and categories.
Each product's "Category_id" refernces a category's "Category_id" in the "Product_Category" table.


2nd anwer: In the "Products" table to ensure that each product is assigned to valid category, we can enforce the foregin key constraint on the "Category_id" column. 
This will ensures us that every value in the "Category_id" column of the "Products" table must exist as a primary key in the "Category_id" column of the "Product_Category" table.
If a product is inserted or updated with a category that does not exist in the "Product_Category" table, the database will raise a foregin Key contraint violation error.
