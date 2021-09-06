# ETG-IMS-Project
Inventory Management System created under ETG's skill india python for ML/AI internship
### This inventory management system emulates the working of an inventory management system in a pharmacy
This inventory management system project consists of 2 files for adding new products to the inventory and for purchasing products that are available in the inventory.
It uses a NO-SQL database for storing the product details, namely JSON. There are 2 files, record.json and sales.json to indicate the products available in the inventory as well as the total sales made respectively.

## Add New Products.ipynb
- Reads the data from record.json and stores it in a python dictionary
- User interface to add new products in the inventory iteratively
- If a match is found in the product ID, the user is prompted to increase the quantity of the specific product or retry

## Purchase Products.ipynb
- Reads the data from record.json and stores it in a python dictionary. Also creates 2 more dictionaries to store the total sales value and bill value for each customer
- User interface to view the catalog, purchase products, generate their bills and to reset the bill when the purchase is done.
- Sales details are saved in a file sales.json which is indexed on the basis of the time of purchase
- Generated the catalog and bill requested by the user in a tabular format for easy viewability
- Removes the product from the inventory completely if its quantity reaches 0 after a purchase is made
- Prints separate bills for every customer and also a prints the total number of customers visited when the portal is exited.

## record.json
- NO-SQL database to store the items in the inventory 
- Each medicine in the pharmacy inventory is assigned with a unique product ID
- The database holds the name, manufacturing date, expiry date, price and quantity of each product

## sales.json
- NO-SQL database to store the items purchased during the time the portal was open in a chronological order
- All details of each purchase, namely the product ID, name, manufacturing date, expiry data, price and quantity purchased is stored
- The purchases are indexed by the time they occured.
