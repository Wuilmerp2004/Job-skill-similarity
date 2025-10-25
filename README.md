# Job Similarity 

## Overview
This project explores the question:  
**Which jobs are most similar to one another, and what alternative careers could someone in these roles transition into with minimal retraining?**

By analyzing job postings and their associated skills, we identify relationships between roles and uncover possible career pathways based on overlapping skill sets.

## Dataset
The dataset comes from the [Job Skill Set Dataset](https://huggingface.co/datasets/batuhanmtl/job-skill-set) hosted on Hugging Face.  
Key columns used:
- **category** – the category of the job (e.g., IT, Business Development, Finance, HR).  
- **job_title** – the title of the job position.  
- **job_skill_set** – a list of relevant hard and soft skills for the job.  

## Methods
- **Data Cleaning**: Removed unnecessary columns, standardized casing, and used regex to strip brackets/quotes from skill lists.  
- **Feature Representation**: Used `CountVectorizer` to tokenize skills into a matrix.  
- **Similarity Metric**: Applied cosine similarity to measure overlap between jobs.  
- **Queries**: Selected three jobs from different categories and identified their top 10 most similar jobs.  

## Tools & Libraries
- [Hugging Face Datasets](https://huggingface.co/docs/datasets/) – to load the dataset  
- [Pandas](https://pandas.pydata.org/) – for data manipulation  
- [Scikit-learn](https://scikit-learn.org/) – for `CountVectorizer` and `cosine_similarity`  
- [Matplotlib](https://matplotlib.org/) – for data visualization  

## Results
- Identified the top 10 most similar jobs for each of three query jobs.  
- Visualized skill similarity with bar charts to highlight overlapping competencies.  

## Limitations
- Limited coverage in some domains (e.g., missing specialized IT roles like Data Scientist or Software Engineer).  
- Skills are based on job postings only, which may not capture differences in practice.  
- Similarity is purely based on co-listed skills, not on job responsibilities or context.  


---
