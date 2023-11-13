# Mini Project 11: Data Pipeline with Databricks 

---

## **Overview**

This project showcases a robust data processing pipeline using Databricks notebooks and Azure Databricks workflows. The pipeline smoothly progresses through data ingestion, transformation, and analysis stages. Utilizing SQL queries, the project establishes a "prepared_song_data" table with columns like artist name, duration, release, tempo, and more, effectively storing processed data within.

Emphasizing best practices, the project advocates Databricks' recommendation of Delta Live Tables, a declarative interface for constructing resilient, maintainable, and testable data processing pipelines. The project's execution aligns with the guidelines provided in the Databricks guide.

In parallel, the automation of data processing and analysis tasks using Databricks is facilitated through scheduled workflows. These workflows can be triggered based on specific conditions or scheduled at regular intervals, optimizing efficiency and managing large-scale data processing pipelines effectively.


---

## **Workflow pipeline**

I initiated the process by acquiring data on songs, proceed to transform it, and load it into a table. Subsequently, I conducted analyses on the processed data.

Below are visualization of successful data pipeline workflows.

![image](https://github.com/nogibjj/IDS706Mini11/assets/141780408/735f5441-c2d4-4259-9b42-fd4c3896b82f)


---

### **Extract**

In this step, I extracted data from the dataset and store the raw information. This notebook was specifically designed to load and preview the data that will be utilized throughout the remainder of the project, as illustrated below:

![image](https://github.com/nogibjj/IDS706Mini11/assets/141780408/7eb4c961-d428-4692-bd00-558a680d9dc2)


### **Transform**

This notebook is dedicated to the ingestion of data and the establishment of a database named "raw_song_data." The code within this file facilitates the storage of data in the Databricks File System (DBFS).
Subsequently, I process the raw song data by refining and trimming the dataset to achieve my desired song dataset. The modified dataset is then saved into a new data sink.

![image](https://github.com/nogibjj/IDS706Mini11/assets/141780408/d6e31856-ef36-4a3b-9c3e-5a0cd0b8736d)

![image](https://github.com/nogibjj/IDS706Mini11/assets/141780408/10926e26-3ba5-449b-afd1-6e5b025b01dc)


### **Load**

Finally, at this stage, I initiated the loading and querying of the data to ensure the proper execution of all preceding steps. Subsequently, this notebook proceeds to establish a SQL database named "prepared_song_data" using the "raw_song_data" table created in the previous notebook. This database serves as a platform for making modifications or conducting additional analyses conveniently using SQL, without affecting the original dataset.

In conclusion, this notebook is crafted to execute a straightforward query on the newly created table, as illustrated below.

![image](https://github.com/nogibjj/IDS706Mini11/assets/141780408/f9215822-6d36-4dc9-a227-213241828661)
---

### **References**
1. https://github.com/nogibjj/python-ruff-template
1. https://docs.databricks.com/en/getting-started/data-pipeline-get-started.html
