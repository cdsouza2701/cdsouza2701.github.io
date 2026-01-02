## Basic Webscraping

**Project description:** This project focuses on building a simple yet reliable web scraping pipeline using Python. The goal was to extract structured information from a publicly available website by sending HTTP requests, parsing HTML content, and isolating relevant data fields.

The project serves as an introduction to collecting raw web data that can later be stored, analyzed, or visualized.

### 1. Problem Statement

Many websites present valuable information in HTML format that is not directly available as structured datasets. Manually copying this data is inefficient and error-prone.

The objective of this project was to:

- Programmatically retrieve web page content

- Understand and navigate HTML structure

- Extract specific data elements consistently and accurately

### 2. Data Source

**Website:** http://quotes.toscrape.com

**Data Type:** Publicly available textual content

**Fields Extracted:**

- Quote text

- Author name

### 3. Methodology

1. **HTTP Request:** Used the requests library to send a GET request and retrieve the page’s HTML content.

2. **HTML Parsing:**
Parsed the returned HTML using Beautiful Soup and the built-in html.parser.

3. **Data Extraction:**
Identified and extracted relevant HTML elements using tag names and CSS class selectors.

4. **Iteration & Output:**
Paired quotes with their corresponding authors and produced clean, readable output for validation.

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
