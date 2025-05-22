# Small to Medium Data Transformation using Pandas

## Overview
In this folder shows an example of using Pandas to transform/clean a small dataset (mock_data.csv) and make it more usable to be uploaded to a data lake and used by a machine learning model (transformed_data.csv). The Python files detail the process of cleaning up the original data using pandas to create the final file.

## Project Structure
```
small-to-medium-data-transformation-pandas/
├── mockdata.py              # Script for generating mock data
├── mock_data.csv            # Original dataset with raw data
├── data-exploration.py      # Initial data exploration script
├── data-cleaning.py         # Data cleaning operations
├── data-transformation.py   # Main transformation script
├── transformed_data.csv     # Final transformed dataset ready for ML
└── .gitignore               # Git ignore file
```

## Data Transformation Process
1. **Input Data**: `mock_data.csv` contains the original dataset with raw data
2. **Exploration**: `data-exploration.py` helps understand the data structure and quality
3. **Cleaning**: `data-cleaning.py` performs initial data cleaning operations
4. **Transformation**: `data-transformation.py` processes the data using Pandas to:
   - Clean missing values
   - Convert data types
   - Handle JSON strings
   - Extract nested fields
   - Standardize formats
5. **Output Data**: `transformed_data.csv` contains the processed data ready for:
   - Upload to data lake
   - Use in machine learning models
   - Further analysis

## Key Operations
- Handling missing values with appropriate strategies
- Converting JSON strings to structured data
- Extracting nested fields from complex data structures
- Standardizing data formats and types
- Ensuring data quality and consistency

## Usage
1. Review the transformation process in the Python scripts:
   - Start with `data-exploration.py` to understand the data
   - Use `data-cleaning.py` for initial cleaning
   - Run `data-transformation.py` for final transformation
2. Refer to `Pandas_cheatsheet.md` for detailed examples of each operation
3. Use `mockdata.py` to generate additional test data if needed
4. Follow the same process to transform your own datasets

## Best Practices
- Always validate data before and after transformation
- Document all transformation steps
- Handle errors and edge cases appropriately
- Ensure data quality meets ML model requirements
- Use appropriate data types for memory efficiency
