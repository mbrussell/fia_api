# Getting FIA data from the EVALIDator API
A repository with resources for gathering data from the [Forest Inventory and Analysis EVALIDator API](https://apps.fs.usda.gov/fiadb-api/evalidator. 

Contains an R Markdown code script that demonstrates how to use the FIA API to gather data from the Forest Inventory and Analysis (FIA) program. The script includes examples of how to access FIA data using the API, as well as how to visualize and analyze the data using R. The example calculates the total acres in Minnesota forests (2022 inventory) by forest type group and ownership group.   

## Parameters in the code
In the *arg_list()* function, you can change values to query  data:

* [snum](https://apps.fs.usda.gov/fiadb-api/fullreport/parameters/snum) is a numeric value representing the attribute of interest (e.g., 2 is for area of forestland in acres).

* rselected is the text for the row grouping variable (e.g, 'Forest type group')
* cselected is the text for the column grouping variable (e.g., 'Ownership group')
* pselected is the text for the page grouping variable. This is optional and can be left blank.
* All of the "selected" grouping variables are [described here](https://apps.fs.usda.gov/fiadb-api/fullreport/parameters/rselected).

* wc is the evaluation group code(s) for inventory(ies) of interest.
* wc typically consists of the state FIPS code concatenated with the 4 digit inventory year (e.g., 272022 for Minnesota, 2022 data)

* The code example will retrieve the area of Minnesota forests (in acres) by ownership group and forest type group. Data for the 2022 inventory. 

* Running this code will provide the same values [as presented here](https://apps.fs.usda.gov/fiadb-api/fullreport?rselected=Forest%20type%20group&cselected=Ownership%20group&snum=2&wc=272022)

# Other resources
* This [FIA Tech Session webinar](https://vimeo.com/861362270/4d996ee479?share=copy) has a good overview of FIA EVALIDator and the API.
* This [blog post](https://arbor-analytics.com/post/2023-10-25-using-r-and-python-to-get-forest-resource-data-through-the-evalidator-api/) describes using the FIA EVALIDator API with R code.
