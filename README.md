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
      - The script loads the XML file specified by input_file (**XML-Schema.xml**) using ET.parse and gets the root element of the XML tree.
  - **Converting XML to a Dictionary**
    - The root element of the XML tree is passed to the xml_to_dict function to convert the entire XML structure into a dictionary format.
    - The xml_to_dict function recursively converts XML elements to a dictionary. If an element has no children, it returns the element's text content. Otherwise, it iterates through the children and constructs a dictionary representing the XML structure.
  - **Converting the Dictionary to JSON Format**
    - The resulting dictionary is then converted to JSON format using json.dumps with an indentation level of 4 for better readability.
  - **Writing the JSON Data to a File**
    - The JSON data is written to a file specified by output_file (**JSON-Schema.xml**) using a file writer (with open statement). The file is saved in the specified path.

![image](https://github.com/user-attachments/assets/1de837e6-250e-42d6-89c7-9b6026b3c488)


### **Explanation of the Script - input_JSON.ipynb**
 - **Loading the JSON File**
   - The script loads the JSON file specified by input_file (**JSON-Schema.xml**) using the json.load function.
 - **Defining the Function to Remove Empty Fields**
   -  The remove_empty_fields function recursively removes empty fields from the dictionary. It handles dictionaries, lists, and basic data types to ensure that no empty fields are left in the resulting JSON data.
  - **Defining the Function to Add Specified Data**
    - The add_data_to_dict function adds specified data to the dictionary. It ensures that nested dictionaries are properly merged and that the new data is integrated into the existing JSON structure.
  - **Specifying the Data to be Added**
    - A dictionary named data contains the information to be added to the existing JSON data. This data includes citation information and material details.
    - This is an example:
![image](https://github.com/user-attachments/assets/a985edba-f565-43db-9aea-91252ff2b5e2)
  - **Adding the Specified Data to the JSON Data**
    - The add_data_to_dict function is used to integrate the specified data into the existing JSON data.
  - **Removing Empty Fields from the JSON Data**
    - The remove_empty_fields function is called to clean the JSON data by removing any empty fields.
  - **Writing the Cleaned JSON Data to a File**
    - The cleaned JSON data is written to a file specified by output_file (**JSON-Input.json**) using a file writer (with open statement). The file is saved in the specified path.

![image](https://github.com/user-attachments/assets/3b97efcb-8733-4a9d-8e7f-02d191e33694)

### Usage Example
- To use these scripts, make sure to update the input_file and output_file paths to your desired file locations.
- Run the **create_JSON.ipynb** script to perform the conversion from XML to JSON and save the output to the specified file.
- Run the **input_JSON.ipynb** script to add specified data to the JSON file, remove empty fields, and save the cleaned JSON data to the specified file.



