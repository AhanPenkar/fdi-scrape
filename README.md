# fdi-scrape
This project scrapes data from the [Department For Promotion of Industry and Internal Trade.] (https://dpiit.gov.in/) It aims to collect all the data that is released in it's quarterly SIA reports and present them in a usable format that is navigable for researchers and investigative journalists.

### Why do this?
In the immediate aftermath of a report released by the Hindenburg group, Adani's offshore accounts were brought under scrutiny. This project aims to make the process of looking into and navigating foreign investment into India more accessible as opposed to parsing and searching PDFs.

## Notebooks
### [1_scraping.ipynb](1_scraping.ipynb)
This is a scraper that collects and downloads all the relavent pdfs from the DPIIT website. It uses BeautifulSoup to find and target quarterly newsletters and the downloads them. 
### [2_process.ipynb](2_process.ipynb)
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

There were several challenges associated with making this project, the first was to do with merging different tables across different years as formatting for it evolved, and the second was to reindex and sort the tables so that they would merge with each other. The pdf to csv conversion was done manually. Ideally, this process would have been automated too. 

### [3_stats.ipynb(3_stats.ipynb)
This has one main function within it ```def searchFor(company)``` which allows users to search for a company in India. It returns all the companies that have invested within in from abroad.
