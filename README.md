# YouTube View Prediction and Correlation Analysis Model

This project focuses on analyzing and predicting YouTube video performance by collecting, cleaning, and modeling view data. The pipeline automates hourly updates of YouTube video metrics, enabling continuous monitoring and evaluation of growth patterns. The analysis explores correlations between views, likes, comments, and other engagement metrics to identify the strongest predictors of video performance.


The project uses a scheduled data collection pipeline to pull new YouTube video metrics every hour:
* Scheduler: A cron job / task scheduler triggers the script on an hourly basis.
* Data Collection: YouTube API (or custom scraper) retrieves video-level statistics such as:
    * Views
    * Likes
    * Comments
*    Watch time
* Storage: Data is appended into a local database / CSV files to maintain historical records.
* Logging: Each run records timestamps and update status for reproducibility.
* This automation ensures that the dataset is always fresh and ready for analysis without manual intervention.
