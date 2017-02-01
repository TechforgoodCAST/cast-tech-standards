# Data Standards

## Data transport format

For a data table, the best format for transporting data is a CSV file (comma separated values). Try
to avoid proprietary formats such as Excel.

Follow good practice when creating CSVs, including:

-	one header row at the top of the file, with column names
-	no blank lines between rows or columns, or before or after a header row
-	separated by commas, with text in quotes
-	dates formatted as "YYYY-MM-DD"

More good tips can be found at <http://www.clean-sheet.org/>

For hierarchical data the best format is usually JSON.

## Identifiers

It's usually preferable to store something using an identifier rather than its name. This helps when
linking data sets together. For example, it's much easier to link charity data when a charity number
is used, rather than using the name which can be written in lots of different ways.

Where possible, use existing identifiers when working with data that could be linked elsewhere. Avoid
using proprietary identifiers (eg use Companies House rather than Dun and Bradstreet numbers for 
companies). Examples of this include:

-	Company Numbers from Companies House
-	Charity Numbers from Charity Commission (/CCNI/OSCR)
-	[ONS geographical codes for areas](https://en.wikipedia.org/wiki/ONS_coding_system) - 
	[list of names and codes](http://geoportal.statistics.gov.uk/datasets?q=Latest_Names_and_Codes&sort_by=name&sort_order=asc)
-	[ISO codes for countries](http://www.nationsonline.org/oneworld/country_code_list.htm)

