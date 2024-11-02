## Data Cleaning and Preparation Process

### 1. Initial Data Assessment
- Reviewed two primary data sources: "verification of Beer Purchaces_Sold - Sheet1.csv" and "Beer Numbers - Sheet1.csv"
- Identified inconsistencies in data structure and formatting

### 2. Data Restructuring
- Transformed data from wide format (months as columns) to long format
- Created a standardized Date/Month column (e.g., 6/2024 format)
- This restructuring facilitated time-series analysis and improved overall data manageability

### 3. Column Additions and Modifications
- Added 'Type' column to distinguish between kegs and cans/bottles
- Created 'Expected Pours' column based on keg/bottle sizes
- Implemented 'Pour Difference' column (Expected Pours - Sold Pours)
- Added 'Expected / Sold Ratio' column for performance analysis

### 4. Data Normalization
- Standardized product names across all entries
- Unified units of measurement (consistently using pours instead of mixing with case or keg counts)

### 5. Handling Missing and Zero Values
- Addressed entries with zero Expected or Sold Pours
- Added placeholder dates (marked in red) for entries missing date information
- Ensured all sold pours were accounted for, even without specific dates

### 6. Calculation Implementations
- Developed formula for Expected Pour Count based on keg sizes:
=IF(H2=13.2, 141G2, IF(H2=15.5, 165G2, IF(H2=5.16, 55G2, H2G2)))
Copy- Calculated Pour Ratio (initially Expected Pours / Sold Pours, later inverted to Sold Pours / Expected Pours)

### 7. Data Verification Process
- Conducted thorough comparison between original and transformed datasets
- Verified product names, dates, pricing, keg sizes, and counts
- Confirmed accuracy of UpPrice/per and discount amounts
- Checked completeness of data transfer and additional calculated fields

### 8. Handling Problematic Data
- Temporarily excluded PU$ column due to difficulties with cell references
- Noted inventory tracking uncertainties for future clarification

### 9. Aggregation and Summary
- Created summary rows for totals to provide quick insights into overall performance
- Implemented running averages for smoother trend analysis

### 10. Data Anonymization for Portfolio
- Replaced actual product names with fictitious beer names
- Ensured anonymized data maintained realistic patterns and relationships

### 11. Extended Date Range (for demonstration purposes)
- Added more dates to the fictionalized dataset to showcase dashboard capabilities over a longer period

### 12. Final Data Validation
- Performed a final check to ensure all calculations were accurate
- Verified that anonymized data reflected realistic business scenarios

### 13. Documentation
- Maintained detailed notes on all data cleaning and transformation steps
- Documented assumptions made during the cleaning process for future reference

This comprehensive data cleaning process ensured the final dataset was consistent, accurate, and well structured for analysis in Google Looker Studio. The process addressed various data quality issues while preparing the data for effective visualization and analysis.