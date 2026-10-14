## Data Transformation: 

●	Restrict the "List of Orders" table to only the first 500 row: **Using the Keep Top Row option in Power query**
●	Ensure the “Order Date” column in the “List of Orders” table is set to data type 'Date': **On top menu click column tools – data type – Select Date**
●	Change the data type of “Amount” and “Target” columns to ‘Fixed Decimal Number’:  **I selected amount profit target column > Transform > Data type >Fixed Decimal Number**
●	Format the "CustomerName" column into proper case, ensuring consistent capitalization for each word : **I selected Customer name column > Transform > Format > Capitalize each word** 
●	Merge the "State" and "City" columns to create a new column named "Location" in the format ‘City, State’ : **we can able to change this using the merge option in Power query** 
●	Create a new custom column named "Profit Margin" as the percentage of "Profit" divided by "Amount".  : **Add column > Custom column Name = Profit / amount then changed data type to %**
●	Add a new conditional column named "Profit Status" based on the values in the "Profit" column. The conditions are as follows: if the profit is less than 0, the label should be "Loss"; if the profit equals 0, the label should be "Break-Even"; and if the profit is greater than 0, the label should be "Profit":

==========================================================================
## Merging Data (Joins): 

●	Merge the "List of Orders" and "Order Details" tables into a new single table named "Orders Data" based on the "Order ID" relationship : **Top menu : Home > Merge Queries > Merge queries as New**
==========================================================================
## Handling Missing Data & Duplicate Data: 

●	Identify missing values in the data and determine a strategy to address them: **I checked all the columns in power query. The column quality shows as 100% and error 0% if there is any null value that will be replaced based on the criteria**

●	Check for duplicate rows and define a strategy to handle duplicates: **Remove rows – remove duplicates to remove duplicate orders**

=========================================================
## Sorting and Filtering Data: 
●	In the ‘Orders Data’ table, utilize sorting and filtering techniques on columns like Order Date, State or Category to analyze data based on specific criteria: 
◆ Sort the orders by Order Date in descending order to analyze recent trends: **Click on order date arrow > Sort Descending**

◆ Filter the orders to focus only on a specific state (e.g., Tamil Nadu) for regional analysis: **Click on state arrow > select Tamil Nadu**

======================================================
## Grouping and Aggregating Data: 

●	Duplicate the “Order Details” table and calculate the count of each Order ID, average profit by Category or total amount by Sub-Category: **Right Click Duplicate > Grouped by Category** 
●	Duplicate the “Sales Target” table and aggregate the total target amount by Month of Order Date : **Duplicated the table > Grouped by Month of Order date and calculated sum of target Amount to get Monthly target**

================================================
## Data Modeling: 
●	Establish a relationship between the “List of Orders” and “Order Details” tables using the ‘Order ID’ column: **List of Orders (Order Id) to many order details (Order ID)**

●	Build a relationship between the “Order Details” and “Sales Target” tables based on the ‘Category’ column. Click "Manage relationships" and ensure this relationship is active: **Order Data based on Order ID ( Category)**
