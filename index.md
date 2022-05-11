# Data Dictionary Minimal Information Model - DDMIM
Medical data is collected and processed in different scenarios, to different extents and in different formats. In order to gain a sufficient impression of these data and their meaning as an outsider, a data dictionary or codebook can be consulted. However, these are not always available and if they are, they are often not standardized, both in terms of content and structure.

The goal of this workshop is to develop a Minimal Information Model for Data Dictionaries, i.e. a vocabulary of consensual concepts and suggestions for obligation. For this purpose, existing Data Dictionaries will be examined and extracted concepts will be discussed. Together with relevant experts such as medical documentalists, medical data scientists, medical informaticians and biometricians we want to discuss what the minimum requirements for such an information model Data Dictionary should be. Questions of the effort of manual creation of such Data Dictionaries for researchers are also relevant.

In the long term, a formal model should be created taking into account existing standards and systems, consented in a broad community and coordinated with relevant stakeholders.



### Core module:
Minimal information to describe a data element.

| Attribute Name | Description | Cardinality |
|--------------|-------------|----------------|
| identifier | An identifier of the data item that is unique in the collection. | 1..1 |
| Short name | A descriptive name for the data element (often used as label). | 1..1 |
| Long description | A detailed description with all relevant information that allows a correct interpretation, especially for third parties. | 1..1 |


### Data quality module:
Minimal information to describe the data quality aspects of a data element.

| Attribute name | Description | Cardinality |
|--------------|-------------|----------------|
| Data type | The data type of the data element value, e.g. numeric, text, date, ... | 1..1 |
| Value Range/ Format | The range of valid values for the data element | 1..1 |
| Unit of measurement | Unit of measurement of a characteristic of the data element corresponding to the value range, e.g. kg, cm; at best standardized, e.g. UCUM | 0..1 |


### Standardization module:
To avoid interpretation errors and simplify machine processing, the annotation of unique codes is helpful.

| Attribute name | Description | Cardinality |
|--------------|-------------|----------------|
| System, Code | A list of codes that classify the information represented by the data element within a conceptual system, specifying the respective associated coding system (e.g., terminology such as Snomed CT, classification such as ICD-10) | 0..n |
