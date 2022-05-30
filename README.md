# Data Dictionary Minimal Information Model - DDMIM
With this project we are attempting to develop a harmonised description of the variables in a data set for medical data bodies.

### Problem description
The problem becomes particularly apparent when persons other than the data originator are to work with the data. 
In that case, an attribute like "name" is not sufficiently unique:

Are we talking about a variable name in the sense of a technical code in the database? What format can/should it have (characters, length)? 
Is it unique? In which namespace? Is it referenced externally?

Are we referring to a name in the sense of a (short) description that should be interpretable by humans? 
How long should/could it be (especially with regard to the display in a GUI)? Are whitespace characters a problem? In which language is it described?
