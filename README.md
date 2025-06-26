```markdown
# Aigeon AI Google Job Search

Aigeon AI Google Job Search is a Python-based server application designed to facilitate job search operations using Google's job search capabilities. This application leverages the SerpApi to perform searches and retrieve job listings based on various parameters such as location, language, and more.

## Features Overview

This project offers a comprehensive tool for scraping Google Jobs search results. It is built on top of the FastMCP framework, providing a robust and efficient server environment. The application is designed to handle multiple parameters to refine and customize job search queries, making it a versatile tool for job seekers and developers alike.

## Main Features and Functionality

- **Google Jobs Search Integration**: Utilizes the SerpApi to perform searches on Google Jobs, allowing users to retrieve job listings based on specific criteria.
- **Customizable Search Parameters**: Supports a wide range of search parameters including query, location, language, domain, and more, enabling precise and targeted job searches.
- **Pagination Support**: Includes functionality to handle pagination, allowing users to retrieve multiple pages of search results.
- **Cache Management**: Offers options to manage caching behavior, either utilizing cached results for efficiency or forcing fresh searches for up-to-date information.
- **Asynchronous Search Capability**: Provides an option to perform asynchronous searches, enabling users to submit queries and retrieve results at a later time.

## Main Functions Description

### `search_job`

The `search_job` function is the core component of this application, responsible for executing job search queries. It accepts several parameters to customize the search:

- **q**: The query string defining the job search criteria.
- **location**: Specifies the geographical location for the search. If omitted, the search may default to the proxy's location.
- **uule**: An encoded location parameter for more precise location-based searches.
- **google_domain**: Defines the Google domain to use for the search, defaulting to google.com.
- **gl**: Specifies the country code for the search, allowing for country-specific results.
- **hl**: Sets the language for the search results.
- **next_page_token**: Used for pagination to retrieve subsequent pages of results.
- **lrad**: Defines the search radius in kilometers.
- **uds**: Enables additional filtering of search results based on Google's filters.
- **no_cache**: Determines whether to use cached results or force a fresh search.
- **aasync**: Controls whether the search is performed synchronously or asynchronously.

The function constructs a payload with the provided parameters, sends a GET request to the SerpApi, and returns the JSON response containing the job listings.

### Server Execution

The server is configured to run using the FastMCP framework, listening on a specified port (defaulting to 9997 if not provided). The server operates using standard input/output for communication, making it suitable for integration into various environments.

This application is ideal for developers and job seekers looking to automate and enhance their job search processes using Google's powerful search capabilities.
```