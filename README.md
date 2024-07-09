# MaterialsMine_XMLconvert

## Convert XSD to XML - **create_XML.ipynb**

### **Prerequisites**
  - Python 3.x
  - xmlschema library
      - pip install xmlschema
  
### **Explanation of the Script**
  - **Reading and Modifying the XSD File**
    - The script reads the content of the XSD file specified by xsd_file_path (**XSD-Schema.xsd**).
    - It uses a regular expression to modify element names that do not conform to XML naming rules (element names starting with a digit).
  - **Writing the Modified XSD File**
    - The modified XSD content is written to a new file specified by modified_xsd_file_path (**Modified-XSD-Schema.xsd**).
  - **Loading the Modified XSD Schema**
    - The modified XSD file is loaded using the xmlschema library.
  - **Generating the XML Structure**
    - The script defines a recursive function generate_element_structure to create the XML structure based on the XSD definitions.
    - It gets the root element name from the XSD schema and generates the XML structure starting from this root element.
  - **Writing the Generated XML to a File**
    - The generated XML structure is converted to a string and written to a file specified by output_file (**XML-Schema.xml**).
        ![image](https://github.com/jhyang13/MaterialsMine_XMLconvert/assets/98197333/ac69894e-1122-4e02-9062-f85e6d8c9c5e)


## Input Data to XML schema - **input_XML.ipynb**

### **Prerequisites**
  - Python 3.x
  - xml.etree.ElementTree

### **Explanation of the Script**
 - **Loading the Existing XML File**
   - The script loads the XML file specified by input_file (**XML-Schema.xml**) and parses it into an XML tree structure.
 - **Adding Data to Elements**
   - The add_data_to_element function recursively traverses the XML tree and adds data to elements based on the provided dictionary.
   - **Specify the data to be added**
     - **'Title', 'Author', 'Citation Type' and 'Publication Year' are required terms** (Pin Tolu)
     - This is an example:
         ![image](https://github.com/jhyang13/MaterialsMine_XMLconvert/assets/98197333/6980e95f-155d-4a67-b57c-a3eb791d1ed5)

 - **Removing Empty Elements**
   - The remove_empty_elements function recursively traverses the XML tree and removes elements that do not contain any text or child elements.
 - **Writing the Modified XML to a File**
   - The modified XML tree is written to a new file specified by output_file (**XML-Input.xml**), with an XML declaration at the top.
     ![image](https://github.com/jhyang13/MaterialsMine_XMLconvert/assets/98197333/1ff7e212-c634-4f74-a42a-d9255d031574)




