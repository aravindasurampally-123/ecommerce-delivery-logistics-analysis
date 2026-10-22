E-commerce Delivery & Logistics Performance Analysis
An end-to-end data analytics project exploring e-commerce delivery
performance, late deliveries, delivery duration, cancellations, product
categories, seller patterns, and customer review scores using Python in
Google Colab and Power BI.
Project Overview
Delivery reliability affects customer experience and logistics
operations. This project analyzes historical e-commerce order data to
measure delivery performance, identify patterns associated with delays,
and present the findings in a Power BI dashboard and final report.
Project Objectives
- Audit and prepare the dataset for analysis.
- Explore the dataset and validate key fields.
- Define and calculate delivery performance KPIs.
- Analyze late-delivery patterns over time and across product
  categories and sellers.
- Compare customer review scores for on-time/early and late
  deliveries.
- Build a Power BI dashboard and summarize practical follow-up
  actions.
Tools Used
- Python --- data preparation and analysis
- Pandas / NumPy --- data manipulation and calculations
- Matplotlib --- charts and visual exploration
- Google Colab --- notebook-based analysis
- Power BI Desktop --- KPI cards and dashboard visualizations
- GitHub --- version control and project documentation
Dataset
The project uses the public Brazilian e-commerce dataset commonly known
as the Olist dataset. The analysis uses order and related data needed to
study purchase dates, delivery dates, estimated delivery dates, order
status, product categories, sellers, and customer review scores.

The analysis does not have a usable carrier identifier or direct
delivery-distance measure, so carrier-level and distance-based
comparisons are not included.
Project Workflow
Week 1 --- Data Quality Audit and Exploratory Data Analysis
- Loaded and inspected the source data.
- Checked dataset shape, data types, duplicate order IDs, missing
  values, and date fields.
- Explored the main order and delivery fields.
- Documented data quality considerations before KPI calculations.
Week 2 --- KPI Engineering and Delivery Performance
- Calculated delivered-order counts and delivery duration.
- Compared actual delivery dates with estimated delivery dates.
- Measured late-delivery and cancellation rates.
- Reviewed monthly late-delivery patterns.
- Compared late-delivery rates across product categories and sellers,
  with attention to sample sizes.
- Compared customer review scores for late versus on-time/early
  deliveries.
Week 3 --- Deeper Analysis and Operational Recommendations
- Examined where late deliveries were more concentrated.
- Compared purchase-to-carrier handover time with carrier-to-customer
  transit time.
- Interpreted the relationship between late delivery and review
  scores.
- Prepared practical follow-up actions and noted the limits of the
  available data.
Week 4 --- Power BI Dashboard and Final Documentation
- Created a Power BI dashboard with KPI cards and charts.
- Prepared a revised project report with findings, limitations, and
  recommendations.
- Documented the workflow and final results for GitHub.
Key Findings
The following figures are from the current analysis summary and should
be interpreted in the context of the available dataset and filters.
  Metric                                                           Result
  Total orders in the orders                                       99,441
  table                          

  Delivered orders eligible for                                    96,470
  actual-versus-estimated
  delivery analysis              

  Late deliveries                                                   6,534

  Late-delivery rate                                                6.77%

  On-time or early deliveries                                      93.23%

  Average purchase-to-customer                                 12.56 days
  delivery duration              

  Median purchase-to-customer                                  10.22 days
  delivery duration              
  Cancellation rate                                                 0.63%
Additional observations:
- Purchase-to-carrier handover averaged approximately 3.23 days
  among valid non-negative intervals.
- Carrier handover-to-customer transit averaged approximately 9.33
  days among valid non-negative intervals.
- March 2018 had a late-delivery rate of 18.96% in the analyzed
  monthly summary. February 2018 and November 2017 were also
  higher-delay months in that summary.
- Late deliveries were associated with lower customer review scores:
  approximately 2.27 for late orders versus 4.29 for
  on-time/early orders in the matched review subset. This is an
  association, not proof that delay alone caused the lower scores.
- Some seller/category rates are based on relatively small numbers of
  eligible orders. Review the underlying counts before treating a high
  rate as a stable performance ranking.
Power BI Dashboard
The dashboard includes:
- Total Delivered Orders: approximately 96.47K
- Late Delivery Rate: 6.77%
- Average Delivery Duration: 12.56 days
- Monthly late-delivery rate trend
- Late-delivery rate by product category
- Late-delivery rate by seller
The dashboard is intended to support exploration of delivery
performance. Always check the eligible order count alongside rates,
especially for sellers or categories with smaller samples.
Recommendations
1. Investigate operational conditions around months with unusually high
   late-delivery rates.
2. Review the order processing and carrier handover stage, since
   processing time is a meaningful part of the overall delivery
   timeline.
3. Monitor seller and category results together with eligible order
   counts to avoid overreacting to small samples.
4. Track customer review scores alongside delivery performance as a
   customer-experience signal.
5. In future analysis, include carrier, region, and distance data if
   reliable fields become available.
Limitations
- The dataset does not provide a usable carrier identifier or direct
  delivery-distance measure for this analysis.
- Seller and product-category comparisons can be affected by different
  order volumes and product mixes.
- The review-score comparison is observational and does not establish
  causation.
- KPI values depend on the specific eligible records and filters used
  for each calculation. The final notebook and dashboard should be
  treated as the detailed calculation sources.
Repository Contents
The repository currently includes the Week 1 EDA notebook and Week 1
project archive. Add or keep the following deliverables in the
repository as applicable:
- 01_data_quality_eda.ipynb --- original Week 1 notebook, if
  retained separately
- Combined Weeks 1--3 .ipynb notebook --- the full analysis workflow
- week1_project_files.zip --- Week 1 supporting files
- Ecommerce_Delivery_Logistics_Performance_Analysis.pbix --- Power
  BI dashboard
- Ecommerce_Delivery_Logistics_Performance_Analysis_Report_Revised.docx
  --- final report
- README.md --- project documentation
File names in the repository should match the names you actually
upload. If the combined notebook has a different filename, keep its
real filename in the repository and update this list accordingly.

How to Review the Project
1. Open the combined analysis notebook in GitHub or download it and run
   it in Google Colab.
2. Open the .pbix file using Power BI Desktop to explore the
   dashboard.
3. Read the revised report for the methodology, findings,
   recommendations, and limitations.
Author
Aravinda Surampally
