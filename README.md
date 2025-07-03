# DSA-CASE-STUDY-ONE
## Building a Portfolio for a DSA-Case Study on Amazon Product 
After the dataset was given, the first thing i did was to structured the dataset by given it a table by (ctrl-T), click ok.
Then Column B was clean by using this formular =TRIM(LEFT(B18, FIND(" ",B18, FIND(" ",B18, FIND(" ",B18)+1)+1))) on a new Column C and titled Product_Name2, then 
double clicking the right-corner-down to effect the formular on the Column C. The Category Column was cleared to on new Column E and named Top Category with this formular =LEFT(D2, FIND("|", D2 & "|") - 1) and double click the down corner to effect the command on that column. Click any where of the dataset and go to Insert at the Ribbon, then click on the PivotTable, it will open a default dialogue box, click ok and it will open a fresh sheet with a pivot interface. 

Question 1. What is the average discount percentage by product category? 
In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag Discount_Percentage into the Values area. Then right click it move the cursor to summarize value by, then average and click.
o	Home on the Ribbon Tab, click on the % sign after highlighting the Average Discount_Percentage

2. How many products are listed under each category?
	In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag Product ID into the Values area. Then right click it move the cursor to summarize value by, then count and click.

3. What is the total number of reviews per category?


   
5. Which products have the highest average ratings? 
6. What is the average actual price vs the discounted price by category? 
7. Which products have the highest number of reviews? 
8. How many products have a discount of 50% or more? 
9. What is the distribution of product ratings (e.g., how many products are rated 3.0, 
4.0, etc.)? 
10. What is the total potential revenue (actual_price × rating_count) by category? 
11. What is the number of unique products per price range bucket (e.g., <₹200, 
₹200–₹500, >₹500)? 
12. How does the rating relate to the level of discount? 
13. How many products have fewer than 1,000 reviews? 
14. Which categories have products with the highest discounts? 
15. Identify the top 5 products in terms of rating and number of reviews combined.
