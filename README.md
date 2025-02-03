This repository was created to store Homework 4 from DATA 601 from University of Calgary's Data Science and Analytics course.
In this project, we used Regular Expressions (RegEx) to extract data from columns such as:
1. Data in a Wrong format: numerical fields were stored as object due to mismatching in data format
2. Standardize Postal Code: the column postal code was not on the correct format (A1A 1A1) and Regular expressions were useful to correct and standardize this.
3. Extract from 'Property Name' items that do not seem to be Public Places (different from the majority of the dataset). The keywords used were: ['Centre','Arena','Building','Station','Warehouse','Depot','Headquarters','Office','Service','Facility','Complex','EMS','School']
4. Correct and standardize Address abbreviations: some addresses were wrongly abbreviated (such as: Av for Avenue, Ga for Gate, etc.). Regular expressions were used to correct this.

