PostgreSQL: 
This project is designed to assist job seekers like me in finding the right data-related job opportunities.
Utilizing PostgreSQL, the project aggregates and analyzes various job listings, allowing users to filter and explore positions based on their specific needs and qualifications. 
In today’s competitive job market, it's crucial for job seekers to identify opportunities that align with their skills and career goals. 
This project aims to simplify that process by providing a comprehensive database of job listings that includes essential details such as experience requirements, location, company names, and more. 

Question 1: What are the top-paying data analyst jobs that are remote?
SELECT 
  job_id,
	job_title,
  name AS company_name,
	job_location,
	job_schedule_type,
	salary_year_avg,
	job_posted_date
    
FROM 
    job_postings_fact
LEFT JOIN company_dim ON job_postings_fact.company_id = company_dim.company_id
WHERE
    job_work_from_home = TRUE AND
    job_title_short = 'Data Analyst' AND
    salary_year_avg >= 125000
ORDER BY salary_year_avg DESC
LIMIT 5;

Results: 
{
    "job_id": 226942,
    "job_title": "Data Analyst",
    "company_name": "Mantys",
    "job_location": "Anywhere",
    "job_schedule_type": "Full-time",
    "salary_year_avg": "650000.0",
    "job_posted_date": "2023-02-20 15:13:33"
  },
  {
    "job_id": 547382,
    "job_title": "Director of Analytics",
    "company_name": "Meta",
    "job_location": "Anywhere",
    "job_schedule_type": "Full-time",
    "salary_year_avg": "336500.0",
    "job_posted_date": "2023-08-23 12:04:42"
  },
  {
    "job_id": 552322,
    "job_title": "Associate Director- Data Insights",
    "company_name": "AT&T",
    "job_location": "Anywhere",
    "job_schedule_type": "Full-time",
    "salary_year_avg": "255829.5",
    "job_posted_date": "2023-06-18 16:03:12"
  },
  {
    "job_id": 99305,
    "job_title": "Data Analyst, Marketing",
    "company_name": "Pinterest Job Advertisements",
    "job_location": "Anywhere",
    "job_schedule_type": "Full-time",
    "salary_year_avg": "232423.0",
    "job_posted_date": "2023-12-05 20:00:40"
  },
  {
    "job_id": 1021647,
    "job_title": "Data Analyst (Hybrid/Remote)",
    "company_name": "Uclahealthcareers",
    "job_location": "Anywhere",
    "job_schedule_type": "Full-time",
    "salary_year_avg": "217000.0",
    "job_posted_date": "2023-01-17 00:17:23"
  }

Querie EXP.
This job listing provides valuable insights into the expectations and opportunities for a data analyst position,
making it a useful reference for job seekers and professionals in the field.
The combination of role specifics, company details,
and compensation information helps candidates make informed decisions about their career paths.


Question 2: 












  
