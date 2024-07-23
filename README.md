# MaterialsMine_XMLconvert

## **XSD_to_XML** - Convert XSD Schema to XML Schema
  - **XSDtoXML_convert.ipynb**

### **Prerequisites**
  - xmlschema library
      - pip install xmlschema

### **Explanation of the Script - XSDtoXML_convert.ipynb**
  - **Reading and Modifying the XSD File**
    - The script reads the content of the XSD file specified by xsd_file_path (**XSD-Schema.xsd**).
    - It uses a regular expression to modify element names that do not conform to XML naming rules (element names starting with a digit).
  - **Writing the Modified XSD File**
    - The modified XSD content is written to a new file specified by modified_xsd_file_path (**Modified-XSD-Schema.xsd**).
  - **Loading the Modified XSD Schema**
    - The modified XSD file is loaded using the xmlschema library.
  - **Generating the XML Structure**
  - **Writing the Generated XML to a File**
    - The generated XML structure is written to a file specified by output_file (**XML-Schema.xml**).

### Usage Example
- To use these scripts, make sure to update the input_file and output_file paths to your desired file locations.



## **XML_to_JSON** - Convert XML Schema to JSON Schema
  - **XMLtoJSON_convert.ipynb**

### **Prerequisites**
  - json library
  - xmlschema library
      - pip install xmlschema

### **Explanation of the Script - XMLtoJSON_convert.ipynb**
  - **Loading the XML File**
      - The script loads the XML file specified by input_file (**XML-Schema.xml**).
  - **Converting XML to a Dictionary**
    - The root element of the XML tree is passed to the **xml_to_dict function** to convert the entire XML structure into a dictionary format.
  - **Converting the Dictionary to JSON Format**
    - The resulting dictionary is then converted to JSON format using json.dumps.
  - **Writing the JSON Data to a File**
    - The JSON data is written to a file specified by output_file (**JSON-Schema.xml**).

### Usage Example
- To use these scripts, make sure to update the input_file and output_file paths to your desired file locations.



## **JSON_to_XML** - Convert JSON Schema to XML Schema

### **Prerequisites**
  - json library
  - xmlschema library
      - pip install xmlschema

### **Explanation of the Script - JSONtoXML_convert.ipynb**
- **Loading the JSON File**
    - The script loads the JSON file specified by input_file (`JSON-Schema.json`).
- **Recursively Convert Dictionary to XML Elements**
    - The script uses the `dict_to_xml` function to recursively convert the JSON dictionary to XML elements.
- **Creating the Root Element**
    - The script uses the `create_root_element` function to create the root XML element and append all child elements.
- **Converting XML Element Tree to String**
    - The XML element tree is converted to a string using `ET.tostring`.
- **Writing the XML Data to a File**
    - The XML data is written to a file specified by `output_file` (`JSON-to-XML-Schema.xml`).
