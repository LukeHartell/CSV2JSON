# CSV2JSON
Converts a CSV file to a JSON file, using a specified column as the key for each JSON object.

This script uses a function called `convert_csv_to_json` reads a CSV file, strips any leading or trailing whitespace from all cell values, 
and converts the rows into JSON format. The resulting JSON objects use the values from a specified 
main row as keys, ensuring that each entry in the JSON file is uniquely identified by this key.
    
# Args
- `csvFilePath` (str): The path to the source CSV file.
- `jsonFilePath` (str): The path where the output JSON file will be saved.
- `delimiter` (str): The character that delimits the columns in the CSV file. Common delimiters: commas (','), semicolons (';'), or tabs ('\t').
- `mainrow` (str): The column header that will be used as the primary key for each JSON object. This column should uniquely identify each row in the CSV.

# Instructions for CSV File Preparation
- Ensure the CSV file uses the specified delimiter.
- Include a header row with column names at the top of the file.
- The column specified by mainrow should contain unique values for each row to ensure the JSON output is properly keyed.
- Make sure there are no leading or trailing spaces in headers, as this could affect data retrieval.

# Example Usage:
```
convert_csv_to_json(
    csvFilePath = 'path/to/input.csv',
    jsonFilePath = 'path/to/output.json',
    delimiter = ';',
    mainrow = 'id'
)
```
