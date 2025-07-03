# DSA CASE STUDY ONE: Building an Amazon Product Analysis Portfolio
As part of my data analytics journey, I was tasked with analyzing an Amazon product dataset for a Data Structures & Algorithms (DSA) case study. The goal was to transform raw e-commerce data into actionable insights using Excel. Here's the story of how I approached and completed the task step-by-step:

### Step 1: Data Preparation & Cleaning
The first step in any analysis is preparing the data. I began by formatting the raw dataset into a structured Excel table using Ctrl + T, which made sorting and filtering much easier.

### Cleaning the Product Name
To simplify product names, I created a new column Product_Name2 using this formula:
=TRIM(LEFT(B2, FIND(" ",B2, FIND(" ",B2, FIND(" ",B2)+1)+1)))
Then, I double-clicked the fill handle to apply the formula to the entire column.

### Extracting the Top Category
I cleaned the Category column by extracting only the top-level category. This was done in a new column titled Top Category using: =LEFT(D2, FIND("|", D2 & "|") - 1)

### Step 2: Pivot Table Analysis
With the dataset clean, I moved on to creating a Pivot Table from the Insert > PivotTable option, which opened a new worksheet with a blank pivot interface. From here, I carried out multiple analyses:

1. Average Discount Percentage by Category

Rows: Top Category

Values: Discount_Percentage (set to Average by right click it and moving the cursor to summarize value by, then average and click.)

Format: Apply percentage format

2. Number of Products per Category

Rows: Top Category

Values: Product ID (set to Count)

3. Total Reviews per Category

Created a new column Review_Count using: =IF(P2="",0,LEN(O2)-LEN(SUBSTITUTE(O2,",",""))+1)
Refreshed Pivot Table

Rows: Top Category

Values: Review_Count (set to Sum)

4. Products with Highest Average Ratings

Rows: Top Category

Values: Rating (set to Average)

Sorted by highest ratings

5. Average Actual vs Discounted Price

Rows: Top Category

Values: Actual Price, Discounted Price (both set to Average)

6. Products with the Most Reviews

Rows: Top Category

Values: Review_Count (set to Sum)

Sorted by highest values

7. Products with Discounts ≥ 50%

Rows: Top Category

Values: Discount_Percentage (set to Sum)

Filtered or interpreted based on % totals

8. Distribution of Product Ratings

Rows: Rating

Values: Product_Name (set to Count)

9. Total Potential Revenue by Category

New column Potential Revenue:=Actual_Price_Cell * Rating_Count_Cell
Pivot Table:

Rows: Top Category

Values: Potential Revenue (set to Sum)

Format as: #,###.00,,"M"

10. Unique Products per Price Range

New column Price Bucket:
=IF(F2<200, "<₹200", IF(F2<=500, "₹200–₹500", ">₹500"))

Rows: Price Bucket

Values: Top Category (set to Count)

11. Relation Between Rating and Discount

Rows: Rating

Values: Discount_Percentage (set to Sum)

12. Products with Fewer Than 1,000 Reviews

Rows: Review_Count

Values: Review_ID and Rating_Count (set to Count and Sum)

13. Categories with Highest Discounts

Rows: Category

Values: Discount_Percentage (set to Max)

14. Top 5 Products by Rating + Reviews

Rows: Top Category

Values: Review_Count and Rating_Count (set to Sum)

Filter: Value Filters > Top 10 > change to Top 5

### Step 3: Dashboard & Visualization
To present the findings, I designed an interactive dashboard. Key charts and metrics were linked to Slicer Tools, allowing users to filter by categories, price ranges, or ratings. This enabled quick comparisons and dynamic insights.



### Conclusion
This DSA case study helped me apply foundational data analysis techniques using Excel. From data cleaning to advanced pivot table operations and dashboard design, I learned how to extract meaningful business insights from e-commerce datasets. It was not just a technical exercise—but a real-world simulation of how data drives strategic decisions.

![image](https://github.com/user-attachments/assets/e15a0cb1-f76e-4271-ad77-41644bc547fe)
