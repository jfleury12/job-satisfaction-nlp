# Employee Satisfaction Themes
Used unsupervised NLP to analyze web-scraped company reviews, discover common themes of job satisfaction, and quantify their alignment with company core values

<img src="images/cover_photo.jpg" width="800" height="" />

## Background
Currently, when applying for jobs, one of the biggest "black boxes" in the whole job process is knowing what the company culture is like and whether it would be a good fit for you from a community and ethics point of view. It is possible to scour through company reviews, but this usually takes a considerable amount of time.

Secondly, are the companies actually being truthful? It's one thing for a company to receive scathing reviews for bad incentive structures, but if they never promoted that in the first place, it's at least a little forgivable. What is more damning is a complete contradiction between what the employees are saying and what the companies are actively promoting.

## Central Research Questions
* **What are the common reasons why people love or hate their jobs?**
* **Once topics have been idenitified, which companies excel or fail in these categories?**
* **What are the common principles that companies advocate for in their mission/vision statements?**
* **Is there a "mismatch" between what employees believe and what the companies are advocating for?**

## Data Source
The data is sourced entirely from Fortune 100 glassdoor.com company reviews (approximately 250,000+).

## Project Files

**Python Notebooks:**
<br>
[Technical Notebook](https://nbviewer.jupyter.org/github/jfleury12/job-satisfaction-nlp/blob/master/notebooks/technical_notebook.ipynb)
<br>
[Text Preprocessing and Exploratory Data Analysis](https://nbviewer.jupyter.org/github/jfleury12/job-satisfaction-nlp/blob/master/notebooks/text_preprocessing_EDA.ipynb)
<br>
[Web Scraping Script](https://github.com/jfleury12/job-satisfaction-nlp/blob/master/notebooks/data_scraping.ipynb)
<br>

**Presentation:**
<br>
[Presentation Deck](https://github.com/jfleury12/job-satisfaction-nlp/blob/master/Employee_Satisfaction_Presentation.pdf)
<br>

**Python Files:**
<br>
[Python Files](https://github.com/jfleury12/job-satisfaction-nlp/tree/master/python_files)
<br>

## Technical Summary
* Web-scraped 250,000 Fortune 100 company reviews from Glassdoor using BeautifulSoup (~40 hours of scraping)
* Used natural language processing with NLTK and SpaCy to tokenize, POS tag, stem, and remove stopwords from the “Pros” and “Cons” section of each review
* Conducted Topic Modeling using latent dirichlet allocation (LDA) with gensim to extract common topics across “Pros” and “Cons”
* Conducted outlier analysis to identify specific companies that performed extremely well or poorly in job satisfaction topics
* Manually copied and pasted 100 mission statements, purpose/vision statements, core values, and “working with us” pages from company websites
* Used a combination of Topic Modeling and Non-negative matrix factorization (NMF) to extract common topics among company core values
* Used vectorized TF-IDF representations of company values and cosine similarity to compare the “mismatch” between employee sentiment and company core values
