
# RayGargets-Dashboards

### Dashboard Link : https://app.powerbi.com/reportEmbed?reportId=98ce15d7-20f4-49b3-8140-f75aad21e445&autoAuth=true&ctid=ff0f3e3a-3e53-454f-b2b5-6c68753b8ee4
## Problem Statement

This project involves a detailed examination of Ray Gadgets Electronics' sales information through Power BI, designed to inform and refine business tactics by offering detailed insights into product sales, category-based revenue, and market tendencies. It targets a wide range of stakeholders, such as data analysts, corporate leaders, marketing and sales departments, and individuals interested in data analytics and business intelligence. The project illustrates the use of data cleaning, merging, and sophisticated analytical methods to support strategic planning, enhance marketing strategies, and boost sales performance.




### Steps followed 

- Step 1 : Prototype Data Model Creation: Given the transaction dataset initially, I created a prototype data model on excel to dissect the data for better understanding, using it to create fact and dimension tables.
- Step 2 : Data Loading and Transformation: Loaded the dataset into Power BI and used Power Query to clean and format the data, then proceeded to create a data model based on the prototype. Forming a star schema model(one-to-many relationship).
- Step 3 : Measure Creation Using DAX: Utilized DAX functions to create measures that would contain key performance indicators (KPIs) such as total revenue, total profit, and profit margin to aid in calculations and analysis.
- Step 4 : Card visuals were added to the canvas, representing KPIs.
- Step 5 : Initial Data Analysis: Started by analyzing sales data, focusing on high-demand items like smartphones, headphones, and laptops. Identified that operations were predominantly based in Africa and noted that products in the Display and Communication category generated the most revenue.
- Step 6 : Data Update and Integration: Received an updated dataset from February to June, which was added to a previously created folder for the January dataset and then refereshed. This required refreshing in Power BI also for automatic dataset updates, leading to several errors due to issues in the new dataset.
- Step 7 : Data Cleansing: Due to errors and null values in the new dataset, returned to Power Query to clean and organize/format the dataset before proceeding with the report.
- Step 8 : Diagnostic Analysis: Noticed a significant profit drop in May, prompting a diagnostic analysis to explore the reasons behind it. This involved examining the quantity sold and product categories for May, which revealed a decrease in purchases in the Video, Display, and Leisure categories, contrary to growth in the Communication category.
- Step 9 : Profit Margin Analysis: Analyzed profit margins based on months. Used DAX to categorize the Quantity sold into groups of 50s to streamline profitability analysis further.     
- Step 10 : Calculated column was created in the fact table in which, quantity category was grouped.

for creating new column following DAX expression was written;
       
        Quantity Category = 
VAR QuantitySold = 'Fact Table'[Quantity Sold]
RETURN
    SWITCH(
        TRUE(),
        QuantitySold <= 50, "0-50",
        QuantitySold <= 100, "051-100",
        QuantitySold <= 150, "101-150",
        QuantitySold <= 200, "151-200",
        QuantitySold <= 250, "201-250",
        QuantitySold <= 300, "251-300",
        QuantitySold <= 350, "301-350",
        QuantitySold <= 400, "351-400",
        QuantitySold <= 450, "401-450",
        QuantitySold <= 500, "451-500",
        "500+"
    )

Snap of new calculated column ,
![Screenshot 2024-02-22 025007](https://github.com/JaneB00/RayGargets-/assets/160017682/ddef6da2-ec35-4860-b34d-1b2cfdbd9de6)
- Step 11 :Two Slicers were added for Product Name and Quarter.
           Using visual level filter from the filters pane, basic filtering was used & blank values were unselected as they were pretty much ignorable. 
 - Step 12 : Since i have three dashboards containing the different analysis, a navigation button was added. 

 ![Screenshot 2024-02-22 040540](https://github.com/JaneB00/RayGargets-/assets/160017682/805c293c-b983-4f0c-b934-ee5b046a3e3d)
  

 - Step 13 : The report was then published to Power BI Service.
 
 
![Screenshot 2024-02-22 024634](https://github.com/JaneB00/RayGargets-/assets/160017682/d5ef69f2-0e17-4014-9e11-5b4b98080505)

# Snapshot of Dashboard (Power BI Service) first page

![Screenshot 2024-02-22 025639](https://github.com/JaneB00/RayGargets-/assets/160017682/6885a678-4ea0-4999-a4c0-eb38dfb3dd07)

 
 # Report Snapshot (Power BI DESKTOP) first page

 
![Screenshot 2024-02-22 025858](https://github.com/JaneB00/RayGargets-/assets/160017682/5219218e-6ae7-4066-95f9-3d99fb0a3c06)

# Insights And Recommendations
1. Prioritize High-Demand Electronics: Analysis identified smartphones, headphones, and laptops as top sellers in African markets, emphasizing the need to concentrate on these items. Recommendation: Allocate more marketing resources and inventory to these high-demand products to capitalize on their strong sales performance.

![Screenshot 2024-02-22 034815](https://github.com/JaneB00/RayGargets-/assets/160017682/5e9c365e-4b51-4284-a327-bbf043d33f1e)

2. Focus on Revenue-Generating Categories: The Display and Communication categories were pinpointed as the largest contributors to revenue, based on data from January through June. 
Recommendation: Enhance product offerings and promotional efforts in these categories to further boost revenue.

![Screenshot 2024-02-22 035123](https://github.com/JaneB00/RayGargets-/assets/160017682/462e7ab9-37f7-408e-8f67-fe072ae87e5d)


3. Geographic Expansion: Assess the performance in current regions of operation and identify potential for expansion in underrepresented areas, leveraging market research to inform decisions.

![Screenshot 2024-02-22 035139](https://github.com/JaneB00/RayGargets-/assets/160017682/0390042c-fbdc-4536-bf94-ca42d48ca470)

4. Address Data Integration Challenges: Encountered issues with integrating new datasets into Power BI, including errors and null values. 
Recommendation: Implement stringent data validation and cleaning protocols before data integration to maintain report accuracy and reliability.

![Screenshot 2024-02-22 035615](https://github.com/JaneB00/RayGargets-/assets/160017682/2dbda8bb-7f1a-4d87-be29-6442883dedfa)

![Screenshot 2024-02-22 035530](https://github.com/JaneB00/RayGargets-/assets/160017682/0419cdba-82a5-4658-a293-73f253cdc398)

![Screenshot 2024-02-22 035548](https://github.com/JaneB00/RayGargets-/assets/160017682/13982a05-3795-4536-af1b-fbcbb2cb2b59)

5. Analyze Profit Margin Fluctuations: Noted a profit decline from $501 million in April to $377 million in May, primarily due to decreased purchases in Video, Display, and Leisure categories, while Communication saw an uptick. 
Recommendation: Conduct a monthly sales and profit analysis to identify and address the underlying causes of fluctuations, with a focus on April's low profit margin of 30.2% and March's high of 37.5%, to strategize on improving profit margins.
![Screenshot 2024-02-22 035755](https://github.com/JaneB00/RayGargets-/assets/160017682/3867b7a1-5468-42f8-bf51-7d7053d96e97)

![Screenshot 2024-02-22 040300](https://github.com/JaneB00/RayGargets-/assets/160017682/ae4be123-9ad6-4863-bdd3-972a1f988fc3)


#RayGargets dashboards
