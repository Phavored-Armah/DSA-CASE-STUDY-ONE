# DSA-CASE-STUDY-ONE
## Building a Portfolio for a DSA-Case Study on Amazon Product 
After the dataset was given, the first thing i did was to structured the dataset by given it a table by (ctrl-T), click ok.
Then Column B was clean by using this formular =TRIM(LEFT(B2, FIND(" ",B2, FIND(" ",B2, FIND(" ",B2)+1)+1))) on a new Column C and titled Product_Name2, then 
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
 o  	Creat a new column by the Review_ID
 o	Enter this formular=IF(P2="",0,LEN(O2)-LEN(SUBSTITUTE(O2,",",""))+1)
 o	Name it Review_Count
 o	Go to the PivotTable Tool on the Ribbon → Analyze → Refresh
	In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag Review_Count into the Values area. It should be on sum.

4. Which products have the highest average ratings?
   	In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag Rating into the Values area. It should be on sum.
o	Right click and go to sort, then sort by highest to smallest

5. What is the average actual price vs the discounted price by category?
   	In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag both Actual Price and Discounted Price to the Values area.
o	Ensure both are on Average
 
6. Which products have the highest number of reviews?
    In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag Review_Count into the Values area. It should be on sum.
o	Right click and go to sort, then sort by highest to smallest

7. How many products have a discount of 50% or more?
    In the PivotTable Fields panel:
o	Drag Top Category into the Rows area.
o	Drag Discount_Percentage into the Values area. Then right click it move the cursor to summarize value by, then sum and click.
o	Home on the Ribbon Tab, click on the % sign after highlighting the Sum Discount_Percentage
 
8. What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
	In the Pivot Table Fields:
o	Drag Rating  into Rows.
o	Drag product_name into Values. Set it to Count.

9. What is the total potential revenue (actual_price × rating_count) by category?
o	Add a new column to the data and name Potential Revenue.
o	Enter this formular =actual_price_cell * rating_count_cell
   	In Pivot Table Fields:
o	Drag Top Category to Rows.
o	Drag Potential Revenue to Values.
o	Ensure it shows Sum.
o	Highlight Potential Revenue Values and press Ctrl 1 on Keyboard and go to custotm and enter #,###.00,,"M", click ok.
 
10. What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
o	Add a new column called Price Bucket.
o	In the first row, enter this formula =IF(F2<200, "<₹200", IF(F2<=500, "₹200–₹500", ">₹500"))
o	Drag the formula down to apply to all rows
	In Pivot Table Fields:
o	Drag Price Bucket into Rows.
o	Drag Top Category into Values. Make sure the value field is set to Count 

11. How does the rating relate to the level of discount?
    In the Pivot Table Fields:
o	Drag Rating into Rows.
o	Drag Discount_Percentage into Values. Set it to sum.

12. How many products have fewer than 1,000 reviews?
In the Pivot Table Fields:
o	Drag Review_Count into Rows.
o	Drag Review_ID and Rating_Count into Values. Set it to count and sum respectively.
    
13. Which categories have products with the highest discounts?

14. Identify the top 5 products in terms of rating and number of reviews combined.
