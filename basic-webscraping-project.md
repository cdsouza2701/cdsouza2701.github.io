## Webscraping
📓 <a href="https://github.com/cdsouza2701/cdsouza2701/blob/dcbac02185120ad2f3467417b4d66e975318a050/Webscraper.ipynb" target="_blank" rel="noopener noreferrer">View Project Code</a>

**Project description:** This project focuses on building a simple yet reliable web scraping pipeline using Python. The goal was to extract structured information from a publicly available website by sending HTTP requests, parsing HTML content, and isolating relevant data fields.

The project serves as an introduction to collecting raw web data that can later be stored, analyzed, or visualized.

### 1. Problem Statement

Many websites present valuable information in HTML format that is not directly available as structured datasets. Manually copying this data is inefficient and error-prone.

The objective of this project was to:

- Programmatically retrieve web page content

- Understand and navigate HTML structure

- Extract specific data elements consistently and accurately

### 2. Data Source

**Website:** <a href="http://quotes.toscrape.com"target="_blank">http://quotes.toscrape.com</a>


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

### 4. Tools & Technologies

- Python

- Requests

- Beautiful Soup

- HTML (DOM structure & CSS classes)

### 5. Key Learnings

- How HTTP requests retrieve web content programmatically

- How to inspect and navigate HTML document structures

- How to extract repeated elements using class-based selectors

- How to pair related data fields accurately

- Importance of validating scraped data before further processing

### 6. Limitations

- Scraping is limited to a single static page

- Extracted data is printed to the console rather than stored

- Pagination and advanced error handling are not implemented

### 7. Legal & Ethical Considerations

Web scraping is not permitted on all websites and must always be performed in compliance with a website’s terms of service and access policies.

For this project, <a href="http://quotes.toscrape.com" target="_blank">http://quotes.toscrape.com</a> was intentionally selected because it is a publicly available demonstration site created specifically for practicing web scraping. The content is openly accessible, does not require authentication, and permits automated access for educational purposes.

No personal, sensitive, or proprietary data was collected as part of this project.
