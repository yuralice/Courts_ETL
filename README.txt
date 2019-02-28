Project Proposal and Final Report located here: https://docs.google.com/document/d/1zNrylv9xqPk5oydAMCa-IspLluPXsWYzoldcKuat_0w/edit?usp=sharing

ETL Project Initial Proposal -- Courts

My project will combine Trial Court information from Harris County for the year of 2018 with the Appellate Court information for the 1st Court of Appeals for the year of 2018. 

The Trial Court information:
https://www.hcdistrictclerk.com/eDocs/Public/Search.aspx
Information will need to be web scraped, utilizing Splinter to handle the pagination
The Appellate Court information:
http://www.search.txcourts.gov/CaseSearch.aspx?coa=coa01&s=c
Information can be exported to a .xls format, will be read in as csv

My plan is to combine these into MongoDB.

ETL Project Final Report -- Courts

My data sources:
Civil Judges:
https://www.justex.net/Courts/Civil/CivilCourts.aspx

Criminal Judges:
https://www.justex.net/Courts/Criminal/CriminalCourts.aspx

Appellate Info:
http://www.search.txcourts.gov/CaseSearch.aspx?coa=coa01&s=c

Process of Extraction, Transformation, Load:
Appellate court info was able to be extracted via .csv. Criminal and Civil judge information was extracted by scraping each website and specifically pulling out the judge’s name and court number.

Appellate court information was transformed and cleaned in a pandas dataframe. Criminal and Civil judge information was transformed into a pandas dataframe.

All three sets of data were loaded into MongoDB.

I transformed the data as noted above so that I would be able to do direct analyses of the judges by court numbers, with the actual cases. 

I chose the final type of database MongoDB, because it was more flexible for the differing sets of data, and will allow for me to later put in Trial Court data as well.

The collections located in my final Court DB database are: Appellate, Civil Judges, Criminal Judges.

Some hypothetical use cases for the database:
Looking at the types of crimes that are prevalent by court
Looking at judge-specific rulings for various crimes
Looking at judge percentages to determine bias
