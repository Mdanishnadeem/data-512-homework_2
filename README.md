# data-512-homework_1
Reproducibility Homework Data 512 

The goal of this project is to analyse the monthly trends of different articles views on wikipedia based on mobile (divided into application and web) and desktop access.

The dataset is available on https://docs.google.com/spreadsheets/d/1A1h_7KAo7KXaVxdScJmIVPTvjb3IuY9oZhNV4ZHxrxw/edit#gid=1229854301

The API is developed by Dr. David W. McDonald(following four cells are from here). This code is provided under the Creative Commons CC-BY license. Revision 1.2 - August 14, 2023
The API documentation, pageviews/per-article, covers additional details that may be helpful when trying to use or understand this example.

The API request will be made using one procedure. The idea is to make this reusable. The procedure is parameterized, but relies on the constants above for the important parameters. The underlying assumption is that this will be used to request data for a set of article pages. Therefore the parameter most likely to change is the article_title.
Note that this is slightly modified to automate introducing device_type as the function parameter. 

I have accessed the data in three different ways 
1. For Desktop
2. For Mobile-Web
3. For Mobile-App

After extracting this data it was converted into json files and mobile web and mobile app were combined into one json file to retrieve the total views through mobile. Moreover, another json file was created which had views of desktop, mobile-web and mobile-app all combined into one. 

The json file could be found under the following naming conventions. 
1. academy_monthly_cummulative_<start201501>-<end202309>.json
2. academy_monthly_desktop_<start201501>-<end202309>.json
3. academy_monthly_mobile_<start201501>-<end202309>.json

Once these files were created the cummulative json file was converted into a dataframe. The dataframe has the following columns 


1. **project**: This column represents the Wikipedia project or language edition. In our case, it is "en.wikipedia," indicating the English-language Wikipedia.

2. **article**: This column represents the name or title of the Wikipedia article being analyzed
   
4. **granularity**: This column specifys the time granularity at which the data is recorded. In our case, it is "monthly," indicating that the data is aggregated on a monthly basis.

5. **timestamp**: This column represents the timestamp of the data. It is formatted as "YYYYMMDD00," where YYYY is the year, MM is the month, DD is the day, and 00 is presumably the hour (though it is constant at 00).

6. **access_app**: This column indicates the method of access to the Wikipedia article through a mobile app, such as the Wikipedia mobile app. 

7. **access_web**: Similar to the previous column, this one specifies the method of access, but for web access. It specifies "mobile-web," conveying access through a mobile web browser.

8. **agent**: This column represents the user agent or type of user accessing the article. 

9. **views_app**: This column contains the number of page views for the Wikipedia article via the mobile app during the specified time period (monthly).

10. **views_web**: Similar to the previous column, this one contains the number of page views, but specifically for web access through a mobile web browser.

11. **total_views**: This column contain the total number of page views for the Wikipedia article, which is calculated as the sum of views from mobile app, mobile web access and desktop.

12. **access_desktop**: This column specifies the method of access for desktop users

13. **views_desktop**: This column contains the number of page views for the Wikipedia article via desktop access during the specified time period.

14. **views_mobile**: This column contains the number of page views for the Wikipedia article via mobile access, which is likely calculated as the sum of views from both mobile app and mobile web access.

Each row in the DataFrame represents data for a specific time period (monthly) and provides information about page views for the specified Wikipedia article, differentiating between mobile app, mobile web, and desktop access, as well as providing total views. The "timestamp" column indicates the time period to which the data corresponds.

In the end I have created three visualisations which are as follows 
1. Plotted a timeseries graph for articles which has the highest and lowest monthly average views.
2. x
3. This graph picks 10 articles with least data available in terms of months and plots their views for mobile and desktop. 
