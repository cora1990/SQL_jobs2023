
-- In the job_postings_fact table get the columns job_id, job_title_short , job_location , and job_via columns. And order it in ascending order by job_location.
SELECT
	job_id,
	job_title_short,
	job_location,
	job_via
FROM
	job_postings_fact
ORDER BY
	job_location;
   

-- In the job_postings_fact table get the columns job_id, job_title_short , job_location , and job_via columns. And order it in descending order by job_title_short.
SELECT
	job_id,
	job_title_short,
	job_location,
	job_via
FROM
	job_postings_fact
ORDER BY
	job_title_short DESC;
    
    
-- Get the unique job locations in the job_postings_fact table. Return the results in alphabetical order.

SELECT DISTINCT
	job_location
FROM
	job_postings_fact
ORDER BY
	job_location;

-- In the job_postings_fact table get the columns job_id, job_title_short , job_location , job_via , and salary_year_avg columns. Order by job_id in ascending order. And only look at rows where job_title_short is ‘Data Engineer’.

SELECT
	job_id,
	job_title_short,
	job_location,
	job_via,
	salary_year_avg
FROM
	job_postings_fact
WHERE
	job_title_short = 'Data Engineer'
ORDER BY
	job_id;


-- Find all job postings in the job_postings_fact where the job_title includes "Engineer" in it with ONLY one character followed after the term. Get the job_id , job_title, and job_posted_date. Order by job_id in ascending order.
SELECT 
	job_id, 
	job_title,
	job_posted_date
FROM 
	job_postings_fact
WHERE 
	job_title LIKE '%Engineer_'
ORDER BY
	job_id;

-- Identify job postings in the job_postings_fact table where the job_title contains the pattern "a_a" anywhere in the title. Return the job_id and job_title columns. Order by job_id in ascending order.
SELECT 
	job_id, 
	job_title
FROM 
	job_postings_fact
WHERE 
	job_title LIKE '%a_a%'
ORDER BY
	job_id;
