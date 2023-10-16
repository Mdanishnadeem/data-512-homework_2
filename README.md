# data-512-homework_2
Analysis

01_Scraping_HW2.ipynb
Does the initial scraping by getting info of the different pages provided to it

02_Scraping_ORES_HW2.ipynb
Gets the category of the article quality using the lastrevid of each article 

1. FA - Featured article
2. GA - Good article (sometimes called A-class)
3. B - B-class article
4. C - C-class article
5. Start - Start-class article
6. Stub - Stub-class article

03_Joining_Data.ipynb
It joins all of the data sources we have primarily the data coming from the first and second notebook with the population and regional division files.

04_Results.ipynb
This produces embeded tables for all of the required questions 

All of the data used in this analysis is available in this repository

DATA 

1. page_record.csv: this is the processed output of the first jupyter notebook
2. record.json: contains all the scrapped records in raw form
3. ores_predictions.csv: this is the processed output of the second jupyter notebook
4. ORES.json: contains all the scrapped records from second jupyter notebook in raw form
5. join_with_states.csv: this is a temporary file and contains joins of page_record and ores_predictions with states
6. wp_scored_city_articles_by_state.csv: this is the final cleaned output file which contains output in the desired format



### RESEARCH IMPLICATIONS 

From my analysis I have found out that the state with the highest good quality articles per capita is South Dakota. Whereas the division with the highest good quality articles per capita is New England and South Dakota is not a part of New England. This was particularly surprising for me. Moreover the highest number of articles per capita were also from South Dakota this is consistent with having the highest quality articles however surprising as well because even though they had the highest number they had the best quality as well

What biases did you expect to find in the data (before you started working with it), and why?

Before working with Wikipedia data, I expected biases because of the nature of Wikipedia's content generation. Wikipedia is created and edited by volunteers, and as such, biases may arise based on the interests, expertise, and perspectives of those contributors.
Sources of bias can include underrepresentation of certain topics or regions, systemic bias related to gender, ethnicity, and cultural perspectives, and uneven coverage of notable versus non-notable subjects.


What might your results suggest about (English) Wikipedia as a data source?

Wikipedia is a valuable but imperfect data source. Its reliability and completeness can vary significantly across topics. The biases observed may limit its suitability for some research questions or applications.

What (potential) sources of bias did you discover in the course of your data processing and analysis?

I discovered during my analysis that some of the regions were covered more as compared to the other regions

