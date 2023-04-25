# fdi-scrape
This project scrapes data from the [Department For Promotion of Industry and Internal Trade.] (https://dpiit.gov.in/) It aims to collect all the data that is released in it's quarterly SIA reports and present them in a usable format that is navigable for researchers and investigative journalists.

### Why do this?
In the immediate aftermath of a report released by the Hindenburg group, Adani's offshore accounts were brought under scrutiny. This project aims to make the process of looking into and navigating foreign investment into India more accessible as opposed to parsing and searching PDFs.

## Notebooks
### [1_scraping.ipynb](1_scraping.ipynb)
This is a scraper that collects and downloads all the relavent pdfs from the DPIIT website. It uses BeautifulSoup to find and target quarterly newsletters and the downloads them. 
### [2_process.ipynb] (2_process.ipynb)
This takes the CSVs which have been connverted and collates them into one large dataframe. The final dataframe has the following columns:

| Column | Description |
| ------------- | ------------- |
|# | Number used for indexing and collating |
| Quarter | The last month of the corresponding quarter when money was invested |
| Company  | The Indian company which is being invested in |
| State | The state in which the Indian company is located |
| District | The ditrict in which the Indian company is located |
| Item | A description of the company |
| Foreign Collaborator | Name of the Foreign company/investor investing into the Indian company| 
| Country | The country in which the foreign collaborator is located |
| Rupees | Amount invested in Rupees |
| Dollars | Amount invested in Dollars |
| Year | The year the amount was invested | 

