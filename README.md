# Sentiment Analysis on Scraped Text Data

## Project Overview
In this project, we scraped content from various articles hosted on the Blackcoffer website using article URLs provided in a link file. After scraping the data, we performed sentiment analysis using a dictionary to calculate key sentiment scores such as **Positive Score**, **Negative Score**, **Polarity Score**, and **Subjectivity Score**. Additionally, we extracted linguistic features like **Word Count**, **Average Sentence Length**, **Average Word Length**, and **Personal Pronouns**. The entire process is performed programmatically using Python.

## Steps Completed

### 1. Reading the Link File
The project starts by reading a file containing URLs of various articles hosted on the Blackcoffer website. These URLs serve as the input for the scraping process. The link file is typically a CSV or text file containing a list of article URLs.

- **Input**: A CSV or text file with URLs.
- **Example URL**: `https://insights.blackcoffer.com/ensuring-growth-through-insurance-technology/`.

Each URL from the file is processed to scrape its content.

### 2. Performing the Web Scraping Operation
The scraping operation is performed using the `requests` and `BeautifulSoup` libraries in Python. For each URL, the content of the article is fetched and extracted from the webpage. The scraping process involves:

- Sending a request to the URL to retrieve the HTML content.
- Parsing the HTML content using BeautifulSoup.
- Extracting the article's main content (usually found in specific HTML tags).
- Handling exceptions and errors (e.g., if the page is unavailable or malformed).

The content extracted from each article is then stored in a structured way for further processing.

### 3. Creating a DataFrame of Scraped Data
Once the article content is scraped, a DataFrame is created using the `pandas` library. Each row represents a single article, and the columns contain relevant information:

- **URL**: The URL of the article that was scraped.
- **Filename**: The name of the article file.
- **Text**: The content of the article.
- **Number of Sentences**: The total number of sentences in the article.

### 4.Data Preprocessing
- **Text Cleaning**: Cleaned the text by removing any unnecessary characters, formatting issues, and ensuring it was ready for analysis.
- **Text Lowercasing**: Converted all the text to lowercase for consistency and to avoid case-sensitive issues in analysis.

### 5.Sentiment Score Calculation
- **Positive and Negative Scores**: Calculated the number of positive and negative words in the text based on predefined positive and negative word lists.
- **Polarity Score**: Calculated the polarity score as the difference between the positive and negative scores, normalized by the total number of positive and negative words.
- **Subjectivity Score**: Calculated subjectivity as a measure of how subjective the text is, based on the sum of positive and negative words.

### 6.Linguistic Feature Extraction
- **Word Count**: Calculated the total number of words in each article.
- **Average Sentence Length**: Calculated the average length of sentences in each article.
- **Average Number of Words Per Sentence**: Derived the average number of words per sentence in each article.
- **Average Word Length**: Calculated the average length of words used in each article.
- **Personal Pronouns**: Counted the occurrence of personal pronouns in each article.

### 7.Data Visualization
- **Polarity Score Distribution**: Visualized the distribution of polarity scores across the dataset using histograms.
- **Word Count Distribution**: Visualized the distribution of word counts across the dataset using histograms.
- **Sentiment Score Comparison**: Compared the positive and negative scores for each article using bar plots.
- **Subjectivity vs Polarity**: Plotted the relationship between subjectivity and polarity scores using scatter plots.
- **Average Sentence Length**: Visualized the average sentence length for each article using bar plots.
- **Personal Pronouns Count**: Created bar plots to visualize the count of personal pronouns in each article.

## Requirements
- Python 3.x
- Pandas
- Matplotlib
- Seaborn
- BeautifulSoup
- Requests

## Installation Instructions
To run the sentiment analysis and scraping process, follow these steps:

1. Clone this repository.
2. Install the necessary dependencies:
   ```bash
   pip install pandas matplotlib seaborn beautifulsoup4 requests

