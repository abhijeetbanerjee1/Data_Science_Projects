# Job Search Helper:

## Overview
Job Search Helper is a web scraping tool designed to assist users in efficiently finding job postings that match their skills and qualifications. This tool automates the process of searching for relevant job opportunities on a specific website, allowing users to focus their time and effort on applying for positions that align with their expertise.

## Features
- Web scraping: Job Search Helper utilizes web scraping techniques to extract job postings from a designated job website.
- Skill-based filtering: The tool filters job postings based on specific skills provided by the user, ensuring that only relevant opportunities are stored.
- Customizable output: Users can specify the format and location for saving the filtered job postings, facilitating easy access and organization.

## Requirements
- Python 3.8
- BeautifulSoup (bs4)
- Requests

## Files:
- The "home.html" file is a dummy HTML file and the "main.py" performs a test on the HTML file.
- The main_1.py is the actual Job Search Helper which scrapes the website "www.timesjobs.com".
- The "job_postings" folder contains .txt files that the program creates for each new posting it scrapes and the scraping happens every 10 mins.
