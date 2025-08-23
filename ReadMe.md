# AWS Weather API Project

## Why this project?
I wanted to use the knowledge I gained from studying for the DEA-C01 exam to build a pipeline using data pulled from an API.
This gave me the opportunity to use some hands-on experience with several aspects of data handling in AWS that I did not have/

## Process
1. I subcribed to the OpenWeather API.
2. I created a Lambda function to pull the 5-day forecast for my zip code, which is updated every 3 hours.
3. I created an EventBridge rule to trigger the Lambda function every 3 hours.
4. After 24 hours, I had accumulated a set of JSON files in my S3 data bucket.
5. I ran a crawler to catalog the data.
6. I used a Glue job to remove some less interesting or unneeded fields (such as city, country, etc.).
7. I used Athena to query the final table and to make a few additional tweaks to the data, such as renaming further fields.
8. I connected QuickSight to Athena and generated several graphs which give a view of the weather in my area during the relevant period.

## The project design diagram can be found here:

## The visuals produced are here, and are shown below, with commentary.

## Conclusion: The 5-day outlook didn't change much during the period covered, and clouds and rain are definitely dominant.