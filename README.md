# Sales-report
Dashboard using Powerbi and Mysql.
Revenue and Profit base dashobard.

Introduction 
A company sales multiple products cross country.The data provided us was for four years 2017 to 2020.The data contains % tables Sales MArket,Sales Products,Sales Customers,Sales Transactions and sales date.
They want to known where company is getting losses and where the company is getting profit,which state is giving more revenue,profit,and profit contribution %,Revenue contribution %.
so i tried to present.

I have uses Power Quarry to clean the data there where some dupilcate entries in sales transaction table ,I had removed it,there were some entries in "USD", so i convertered in Indian "Rs",There was some empty columns in sales market table so i removed it

Discription
On first page i have shown three KPIs as Revenue,sales Quantity and total profit margin. By using bar chart is I have shown profit contribution % by market ,reveune contribution % by market and profit % by market by using dax.
Dax :Revenue = sum('sales transactions'[sales_amount])
    :profit margin % = DIVIDE([total profit margin],[Revenue],0)
    :Revenue contribution % = DIVIDE([Revenue],CALCULATE([Revenue],ALL('sales products'),ALL('sales customers'),ALL('sales markets')))
    :profit margin contribuation % = DIVIDE([total profit margin],CALCULATE([total profit margin],ALL('sales products'),ALL('sales customers'),ALL('sales markets')))


BY using line chart I had shown Revenue trand chart yearly to show diffrent year wise and month wise i had use slicers fore month and year and tried to give detail information using table chart used customers informations for revenue,profit contribution % by market ,reveune contribution % by market and profit % .

on the next page i tried to show profit for the company i have used same kpis as i use on last page and i have used one parameter for profit target i have set it as if we set parameter on 1% if any state giving profit less than 1% will be giving red colour on bar chart and used line and clustered column chart to compare current year and last year revenue and line showing sum of profit margin and used table to show detail information for customers uisng revenue,profit contribution % by market ,reveune contribution % by market and profit % .

    
    
