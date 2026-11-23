# FedEx Supply Chain Delivery Analysis

## Project Overview
This project analyzes pharmaceutical supply chain shipment data to understand delivery performance, identify factors associated with delays, and explore relationships between shipment characteristics and logistics outcomes.

The analysis focuses on delivery status, shipment modes, destination countries, shipment management teams, planned lead time, Vendor INCO Terms, and shipment weight versus insurance cost.

## Objectives
- Evaluate overall shipment delivery performance.
- Identify shipment modes associated with higher delay rates.
- Compare delivery performance across destination countries.
- Analyze shipment performance by management team and vendor.
- Investigate planned lead time and delivery outcomes.
- Examine Vendor INCO Terms and delivery status.
- Explore the relationship between shipment weight and line-item insurance cost.
- Provide data-driven recommendations to improve supply chain efficiency.

## Business Questions
1. Are shipments managed by specific teams more likely to be delivered on time or experience delays?
2. Does shipment mode (Air, Ocean, Truck, etc.) influence delivery performance?
3. Which destination countries experience the highest shipment delay rates?
4. Which shipment modes have the highest frequency of early, on-time, and late deliveries?
5. Does planned lead time differ across delivery performance categories?
6. Do different Vendor INCO Terms have different delivery outcomes?
7. Is shipment weight associated with line-item insurance costs?

## Dataset
The project uses a pharmaceutical supply chain shipment dataset containing shipment, vendor, destination, logistics, delivery date, weight, freight, and insurance information.

- **Original dataset size:** 10,324 records
- **Final cleaned dataset:** 10,324 rows × 36 columns
- **Data types:** Numerical, categorical, and date/time fields
- **Key features:** Shipment Mode, Country, Vendor, Managed By, Scheduled Delivery Date, Delivered to Client Date, Weight (Kilograms), Freight Cost (USD), and Line Item Insurance (USD)

## Data Cleaning & Preprocessing
- Created a copy of the original dataset for cleaning.
- Converted relevant date columns to datetime format.
- Converted numerical columns to appropriate numeric data types.
- Checked duplicate records.
- Reviewed missing values and handled missing shipment mode values using an `Unknown` category.
- Created delivery delay features.
- Classified shipments as **Early**, **On Time**, or **Late**.
- Calculated planned lead time between PO sent date and scheduled delivery date.
- Validated the cleaned dataset.

## Analysis & Methodology
### Exploratory Data Analysis
- Overall delivery status distribution
- Shipment mode analysis
- Country-level delivery performance
- Shipment management team analysis
- Planned lead time analysis
- Shipment mode delivery-status comparison
- Vendor INCO Terms analysis
- Vendor delivery performance

### Statistical Analysis
- Chi-square tests of independence
- Expected frequency analysis
- Cramér's V effect-size measurement
- Pearson correlation
- Spearman rank correlation

### Visualizations
The project includes multiple visualization types:
- Count plots
- Bar charts
- Histograms
- Boxplots
- Stacked percentage charts
- Scatter plots with trendlines
- Symlog scatter plots

## Key Findings
- **Overall delivery performance:** 61.26% of shipments were on time, 27.26% were early, and 11.49% were late.
- **Shipment mode:** Ocean shipments had a late-delivery rate of 17.52%, followed by Truck at 16.08%.
- **Destination country:** Burundi had the highest late-delivery rate among the countries included in the minimum-volume comparison (38.78%, based on 98 shipments).
- **Management team:** PMO-US managed approximately 99.43% of shipments, so comparisons with other teams were limited by their small sample sizes.
- **Planned lead time:** Late shipments had a higher median planned lead time (107 days) than on-time shipments (92 days), though the distributions were highly variable.
- **Vendor analysis:** Delivery performance varied across vendors. Vendor-level statistical analysis indicated an association between vendor and delivery status.
- **INCO Terms:** The `N/A - From RDC` category had a late-delivery rate of 17.15%.
- **Weight and insurance:** Shipment weight showed a positive association with insurance cost (Pearson correlation: 0.6172; Spearman correlation: 0.7786).

## Business Recommendations
- Monitor Ocean and Truck shipments closely and investigate recurring delay patterns.
- Prioritize destination countries with elevated late-delivery rates for logistics review.
- Develop vendor-level performance monitoring and corrective action plans.
- Review planned lead times and identify shipments with unusual or potentially inconsistent scheduling.
- Investigate shipments categorized as `N/A - From RDC` to improve logistics visibility.
- Use shipment weight as one of the factors in insurance cost monitoring and estimation.
- Continue tracking delivery performance through regular dashboards and KPI reports.

## Tools & Technologies
- **Python**
- **Google Colab / Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SciPy**
- **Statistical Analysis**
- **Data Visualization**

## Project Files
- `FedEx_Supply_Chain_Delivery_Analysis.ipynb` — Complete notebook containing data cleaning, exploratory analysis, visualizations, statistical tests, findings, and recommendations.

## Limitations
- Observational dataset; statistical associations do not establish causation.
- Missing data may reduce the number of valid records in specific analyses.
- Certain categories have small sample sizes, which limits the reliability of comparisons.
- Some scheduling date anomalies were observed, including negative lead times.
- Shipment mode and destination factors may be influenced by other variables not available in the dataset.

## Conclusion
This analysis provides an overview of pharmaceutical supply chain delivery performance and highlights shipment mode, destination, vendor, management, scheduling, and insurance-related patterns. The findings can support targeted logistics monitoring and data-informed operational decisions.

---
**Project Type:** Data Analysis | Supply Chain Analytics | Exploratory Data Analysis | Statistical Analysis
