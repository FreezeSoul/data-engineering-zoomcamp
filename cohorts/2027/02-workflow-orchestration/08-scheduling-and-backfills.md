---
video_url: https://www.youtube.com/watch?v=1pu_C_oOAMA
---
# Local DB: Learn Scheduling and Backfills

We can now schedule the same pipeline shown above to run daily at 9 AM UTC. We'll also demonstrate how to backfill the data pipeline to run on historical data.

Note: given the large dataset, we'll backfill only data for the green taxi dataset for the year 2019.

![A daily schedule processes the latest partition while a separate backfill lane replays historical partitions through the same pipeline](images/08-scheduling-backfill-imagegen.png)
*Scheduling handles new data; backfills reuse the same logic for historical partitions.*

The flow code: [`05_postgres_taxi_scheduled.yaml`](flows/05_postgres_taxi_scheduled.yaml).
