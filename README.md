# Rental Property Scraper and Google Form Automation

## Overview
The `main2.py` script automates the process of scraping rental property listings from a Zillow clone website and submitting the extracted data to a Google Form. This script is particularly useful for users looking to collect and organize rental property information efficiently.

## Tools and Libraries Used
- **BeautifulSoup**: A Python library for parsing HTML and XML documents. It is used in this script to extract data from the web page.
- **Requests**: A simple HTTP library for Python that allows you to send HTTP requests easily. In this script, it is used to fetch the HTML content of the Zillow clone website.
- **Selenium**: A powerful tool for controlling web browsers through programs and automating browser tasks. It is used here to fill out and submit the Google Form.
- **Chrome WebDriver**: A component of Selenium that allows the script to control the Chrome browser.

## Functionality
1. **Web Scraping**:
   - The script sends a GET request to the Zillow clone website using the Requests library, including a user-agent header to mimic a browser.
   - It parses the HTML response with BeautifulSoup to create a structured representation of the page.
   - It extracts:
     - **Links**: URLs to individual property listings.
     - **Addresses**: The physical addresses of the properties, cleaned of unnecessary characters.
     - **Prices**: The rental prices, formatted to remove extraneous text.

2. **Google Form Submission**:
   - The script initializes a Chrome browser instance using Selenium.
   - It iterates through the scraped data and navigates to a specified Google Form URL.
   - For each property, it fills in the address, price, and link fields in the Google Form using XPath to locate the input elements.
   - Finally, it submits the form for each property.

## Usage
To run the script, ensure you have the required libraries installed. You can install them using pip:
```bash
pip install beautifulsoup4 requests selenium
Make sure to have the Chrome WebDriver installed and accessible in your system's PATH.

Conclusion
This script provides a streamlined way to gather rental property data and submit it to a Google Form, saving time and effort in data entry tasks.