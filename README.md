-----

**Situation**

I am working for a company that sells motorcycle parts through three warehouses in the area. The company sells both retail and wholesale and accepts various payment methods (credit cards, cash, and bank transfer), each incurring different fees. The board of directors wants a detailed analysis of wholesale revenue by product line, showing how it varies month-to-month and across different warehouses.


-----

**Task**

My task is to calculate the net revenue for each product line, grouping the results by month and warehouse, and filter the data to include only wholesale orders. I need to present the results in a specific format of

product_line | month | warehouse | net_revenue

to help the board gain better insights into the company’s wholesale performance.

**The Sales Table Schema**

<img src="https://i.imghippo.com/files/RNt881722663862.png">

-----

**Action**

1. Filter Data: Use a WHERE clause to include only rows where client_type is 'Wholesale', ensuring the analysis is limited to wholesale orders.
2. Select Columns: Select product_line, format the month from the date column, select warehouse, and calculate the net_revenue.
3. Format Month: Use the TO_CHAR(date, 'Month') function to display the month in a readable format ('June', 'July', 'August').
4. Calculate Net Revenue: Calculate the net_revenue as the sum of the total column minus the sum of the payment_fee column (SUM(total) - SUM(payment_fee)).
5. Group Data: Group the results by product_line, formatted month, and warehouse using the GROUP BY clause.
6. Order Results: Sort the results by product_line, formatted month, and net_revenue in descending order using the ORDER BY clause.

<img src="https://i.imghippo.com/files/5W2Hv1722670342.png">


-----
**Result**

<img src="https://i.imghippo.com/files/nyxKD1722670620.png">

The query output provides a comprehensive view of net revenue for each product line by month and warehouse. This allows the board to understand the performance of different product lines across different warehouses and months, helping them make informed decisions on inventory management, marketing strategies, and resource allocation. The filtered and calculated net revenue data assists in identifying trends and patterns in wholesale sales, ultimately supporting strategic planning and optimization efforts.
