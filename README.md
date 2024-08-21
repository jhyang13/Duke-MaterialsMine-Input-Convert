# MaterialsMine_Inputconvert

## Overview
This script is designed to automate the process of converting data from an Excel file into XML files, based on a provided XML schema. 
The script is particularly tailored for use with the MaterialsMine platform, facilitating the conversion of data into XML format for further processing or storage.

## Useful Links:

**XSD Schema:** https://qa.materialsmine.org/portal/view-schema
**API Docs:** https://materialsmine.org/api/api-docs/

## Prerequisites
- Python 3.x installed on your system.
- Required Python libraries:
  - pandas
  - xml.etree.ElementTree
  - os
  - re

### Script Configuration
- **Step 1: Change the Input File Header Names**

    The Excel file should have headers that match the corresponding tag names in the XML schema. If a value and unit are needed, the header should be renamed accordingly, e.g., `TensileModulus/unit`, `Other_Processing/ChooseParameter/Drying-Evaporation/Temperature/value`.

- **Step 2: Convert the Input File into XML Files**

  The script reads the Excel file and generates individual XML files based on the provided XML schema. Two specific elements, `SIMULATION-FEA` and `MATERIALPROPERTIES-FEA`, are skipped during the conversion process.

### Output
For each row in the Excel file, the script generates an XML file named using the ID from that row and saves it to the specified output directory. The script also prints a confirmation message for each file created.
  
