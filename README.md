# MaterialsMine_XMLconvert

## Convert XSD to XML - **create_XML.ipynb**

### **Prerequisites**
  - Python 3.x
  - xmlschema library
      - pip install xmlschema
  
### **Explanation of the Script**
  - Reading and Modifying the XSD File
    - The script reads the content of the XSD file specified by xsd_file_path.
    - It uses a regular expression to modify element names that do not conform to XML naming rules (element names starting with a digit).
  - Writing the Modified XSD File:
    - The modified XSD content is written to a new file specified by modified_xsd_file_path.
  - Loading the Modified XSD Schema:
    - The modified XSD file is loaded using the xmlschema library.
  - Generating the XML Structure:
    - The script defines a recursive function generate_element_structure to create the XML structure based on the XSD definitions.
    - It gets the root element name from the XSD schema and generates the XML structure starting from this root element.
  - Writing the Generated XML to a File:
    - The generated XML structure is converted to a string and written to a file specified by output_file.

