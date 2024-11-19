# Data Cleaning and Transformation Process

## Initial Data Assessment and Transformation
The project began with a review of two key datasets, **"Verification of Beer Purchases_Sold"** and **"Beer Numbers"**. Inconsistencies in data structure and formatting were identified, prompting a restructuring effort. The data was converted from a wide format, with months as columns, to a long format with a standardized `Date/Month` column (e.g., `6/2024`). This adjustment allowed for more effective time-series analysis and streamlined data management.

## Enhancing the Dataset
To enrich the dataset, several columns were added:
- A `Type` column to differentiate kegs from cans or bottles.  
- `Expected Pours` based on container sizes, and `Pour Difference` to track discrepancies between expected and sold pours.  
- An `Expected/Sold Ratio` to facilitate performance analysis.  

Product names and units of measurement were standardized for consistency, with all quantities reported as pours rather than mixed units.

## Addressing Data Gaps
Missing or problematic values were handled carefully. Placeholder dates (highlighted for clarity) were added where dates were absent, and zero values in key fields were addressed to ensure no sold pours went unrecorded.

## Calculations and Adjustments
Formulas were developed to calculate expected pour counts based on keg sizes. A pour ratio was initially calculated as `Expected Pours / Sold Pours` before being inverted. Some problematic columns, like `PU$`, were temporarily set aside due to technical challenges, with plans for future resolution.

## Data Verification and Summary
A meticulous verification process compared the original and transformed datasets, ensuring accuracy in product names, dates, pricing, and calculated fields. Summary rows and running averages were included for quick insights and trend analysis.

## Anonymization and Demonstration Enhancements
To prepare the data for portfolio use, product names were replaced with fictional equivalents while maintaining realistic patterns. Additional dates were added to demonstrate dashboard capabilities over an extended timeline.

## Final Validation and Documentation
The final dataset underwent rigorous checks to confirm the accuracy of calculations and alignment with real world scenarios. Every step of the process, along with key assumptions, was thoroughly documented to ensure clarity and reproducibility.

## Outcome
This comprehensive data cleaning process ensured the final dataset was consistent, accurate, and well structured for analysis in Google Looker Studio. The process addressed various data quality issues while preparing the data for effective visualization and analysis.

