# Employee-Data-Transformation
Introduction:
This document serves as a guide to understanding the code for transforming employee data from a columnar format to a historical, row-based versioning format. The code is designed to handle effective and end date calculations, data transformation, and data copying while maintaining unchanged values across different records. It provides detailed explanations of each method and its purpose within the codebase.

#Code Overview:

1. **read_input_csv(file_path)**:
   - Purpose: Reads the input CSV file and returns a pandas DataFrame.
   - Parameters: 
     - file_path: Path to the input CSV file.
   - Returns: 
     - pandas DataFrame containing the data from the input CSV file.

2.identify_and_convert_date_columns(df)**:
   - Purpose: Identifies columns containing the word 'date' (case-insensitive) in their names and converts the values in those columns to datetime format.
   - Parameters:
     - df: pandas DataFrame containing the data.
   - Returns:
     - List of identified date columns.

3. **calculate_tenure(row)**:
   - Purpose: Calculates the tenure (in years) of an employee based on their joining and exit dates.
   - Parameters:
     - row: pandas Series representing a single row of the DataFrame.
   - Returns:
     - Tenure in years (rounded to the nearest whole number).

4. **expand_records(df, date_columns)**:
   - Purpose: Transforms the data into a historical, row-based versioning format.
   - Parameters:
     - df: pandas DataFrame containing the data.
     - date_columns: List of date columns identified for transformation.
   - Returns:
     - New DataFrame containing all the transformed records.

5. save_transformed_data(df, output_file_path)**:
   - Purpose: Saves the transformed DataFrame to a CSV file.
   - Parameters:
     - df: pandas DataFrame containing the transformed data.
     - output_file_path: Path to save the output CSV file.
   - Returns:
     - None.

6. Main Execution**:
   - Purpose: Orchestrates the data transformation process.
   - Steps:
     - Specifies the input and output file paths.
     - Reads the input CSV file.
     - Identifies and converts date columns.
     - Transforms the data into a historical format.
     - Saves the transformed data to the output CSV file.
     - Prints a success message with the location of the output file.

**Usage:**

To use the code for transforming employee data, follow these steps:

1. Ensure Python and required libraries (e.g., pandas) are installed.
2. Provide the input CSV file path and output file path in the code.
3. Run the script.
4. Check the output CSV file for the transformed data.

**Conclusion:**

The code provided offers a robust solution for transforming employee data into a historical, row-based versioning format. By following the guidelines outlined in this document, users can easily understand and utilize the code for their data transformation needs.
