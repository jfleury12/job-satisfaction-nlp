# Employee Satisfaction Themes
![Office Space](https://thumbs.gfycat.com/CheerfulMassiveDrafthorse-small.gif)

Used unsupervised NLP/NLU to analyze web-scraped company reviews, discover common themes of job satisfaction, and quantify their alignment with company core values

- Web-scraped 250,000 Fortune 100 company reviews from Glassdoor using BeautifulSoup (~40 hours of scraping)
- Used natural language processing with NLTK and SpaCy to tokenize, POS tag, stem, and remove stopwords from the “Pros” and “Cons” section of each review
- Conducted Topic Modeling using latent dirichlet allocation (LDA) with gensim to extract common topics across “Pros” and “Cons”
- Conducted outlier analysis to identify specific companies that performed extremely well or poorly in job satisfaction topics
- Manually copied and pasted 100 mission statements, purpose/vision statements, core values, and “working with us” pages from company websites
- Used a combination of Topic Modeling and Non-negative matrix factorization (NMF) to extract common topics among company core values
- Used vectorized TF-IDF representations of company values and cosine similarity to compare the “mismatch” between employee sentiment and company core values
