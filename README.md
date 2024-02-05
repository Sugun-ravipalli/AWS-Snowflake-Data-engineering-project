# Spotify Data Engineering End-to-End Project (AWS + Snowflake)

## Motivation
After encountering challenges with GCP's data engineering pipeline, this project aimed to build a comprehensive end-to-end data engineering pipeline using AWS services. The primary focus was on understanding core services such as Lambda, S3, Athena, and CloudWatch, with an exploration of third-party integration into Snowflake using Snowpipe.

## Architecture Diagram
![Spotify DE AWS architecture](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/c8ac9f25-7261-4474-b0b9-122a7610a3c5)


## Implementation Steps
1. **Spotify API Integration:** Utilized Python Jupyter notebooks for data analysis and segregation into three tables: artist, album, and songs.
   ![python code](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/3e519c41-83c3-4628-8d8b-8ebaffe241d7)

2. **AWS Lambda for Extraction:** Deployed extraction code on AWS Lambda to fetch data directly from the Spotify API to an S3 bucket.
![extraction](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/5d524642-48f5-411b-a725-c65a16c48cf1)

3. **CloudWatch Trigger:** Configured AWS CloudWatch triggers to execute the extraction process automatically every minute.

4. **Transformation Function:** Implemented a Lambda function for data transformation, automating the loading of transformed data to an S3 location using S3 event-based triggers.
![transformation](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/fa4ace38-02fa-457e-843d-8571e354fca9)

5. **File Organization on S3:** Ensured proper organization of files on S3 for efficient data management.
![Screenshot 2024-02-04 125326](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/c4b20122-62b0-4e9f-95f7-9745742d14c1)

6. **Glue and Athena Integration:** Built analytics tables on data files using AWS Glue and Athena for interactive querying.
![Organising](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/8b525c6b-39dc-4a27-8e04-21dda8fc9e0c)

![Athena](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/a6c8a22f-6d1f-4121-8b47-87479685a35c)


8. **Integration with Snowflake:** Explored third-party storage service integration by integrating S3 and Snowflake through Snowpipe.
![SNOWPIPE](https://github.com/Sugun-ravipalli/AWS-Snowflake-Data-engineering-project/assets/145236879/2442bb97-5bf2-4687-a4c8-44c518a5b07a)

# Results and Learnings

This project has been a significant learning curve, particularly in handling JSON data formats. The majority of the heavy lifting was accomplished during the initial data analysis and data transformation stages. Exploring AWS services like Lambda has provided valuable insights into the advantages of serverless computing.

I delved into intricate concepts such as event triggering for automating pipelines, leveraging AWS IAM roles for robust security practices, and organizing data files in S3 to enhance the understanding of process flows. These aspects stand out as highlights of this project.

A particularly satisfying experience was working on the integration of transformed files in S3 to Snowflake through Snowpipe. This process not only demonstrated the seamless integration of different technologies but also provided a practical understanding of working with diverse tech stacks. Following the Snowflake documentation and leveraging online resources, especially YouTube, bridged gaps and facilitated a smoother learning journey.

## What's Next

After this exciting journey, my next focus is on deepening my understanding of data warehousing concepts. Over the next two months, I plan to delve into snowflaking, aiming to complete my project by April.

## Future Enhancements

As part of future enhancements, I plan to explore the integration of data visualization tools such as Amazon QuickSight and Power BI with the data warehouse. This addition will further enrich the analytical capabilities of the project.


