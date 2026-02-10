# readCensusExcel.py

**Code Analysis: `readCensusExcel.py`**

**Description:**

The `readCensusExcel.py` script is a Python program that reads an Excel file containing census data and generates a new Python file with the aggregated population and number of census tracts for each county.

**Functionality:**

1. The script loads an Excel workbook named `censuspopdata.xlsx` using the `openpyxl` library.
2. It extracts data from the "Population by Census Tract" sheet, starting from row 2 (skipping the header row).
3. For each row, it extracts the state, county, and population values.
4. It aggregates the data for each county within each state by:
	* Creating a dictionary `countyData` with state as the key and a sub-dictionary as the value.
	* Within each sub-dictionary, it creates a key for each county and initializes its values to `{'tracts': 0, 'pop':