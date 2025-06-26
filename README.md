# Aigeon AI Google Job Search

## Overview

Aigeon AI Google Job Search is a Python-based server application designed to facilitate job searches using Google's job search capabilities. This application leverages the SerpApi to perform detailed and customizable job searches, providing users with the ability to specify various parameters to tailor their search results.

## Features

- **Customizable Job Search**: Allows users to perform job searches with a variety of customizable parameters such as location, language, and search radius.
- **Integration with SerpApi**: Utilizes the SerpApi to fetch Google Jobs search results, ensuring accurate and up-to-date information.
- **Environment Configuration**: Uses environment variables to manage sensitive information like API keys securely.
- **Efficient Data Handling**: Implements caching mechanisms to optimize search performance and reduce unnecessary API calls.
- **Asynchronous Search Capability**: Supports asynchronous search submissions to improve efficiency and user experience.

## Main Features and Functionality

The application is built around a primary function `search_job`, which is a tool registered with the `FastMCP` server. This function allows users to perform job searches by specifying various parameters:

- **Query (`q`)**: The main search term or query string.
- **Location (`location`)**: Specifies the geographical location for the search, enhancing the relevance of results.
- **Google Encoded Location (`uule`)**: An alternative to `location` for specifying search origin.
- **Google Domain (`google_domain`)**: Allows selection of a specific Google domain for the search.
- **Country (`gl`)**: Defines the country context for the search using a two-letter country code.
- **Language (`hl`)**: Sets the language for the search results.
- **Next Page Token (`next_page_token`)**: Facilitates pagination by retrieving subsequent pages of results.
- **Search Radius (`lrad`)**: Defines the radius for the search in kilometers.
- **Filter (`uds`)**: Applies specific filters to refine search results.
- **Cache Control (`no_cache`)**: Determines whether to use cached results or fetch new data.
- **Asynchronous Search (`aasync`)**: Enables asynchronous submission of search requests.

The function constructs a payload with these parameters and sends a GET request to the SerpApi endpoint to retrieve job search results.

## API Endpoints or Main Functions Description

### `search_job`

This is the primary function of the application, responsible for executing a job search based on user-defined parameters. It constructs a request payload and interacts with the SerpApi to fetch search results. The function returns the JSON response from the API, which contains the job listings and related metadata.

#### Parameters:

- **`q` (str)**: The query string for the job search.
- **`location` (str, optional)**: The location from which the search should originate.
- **`uule` (str, optional)**: Google encoded location for the search.
- **`google_domain` (str, optional)**: The Google domain to use for the search.
- **`gl` (str, optional)**: The country code for the search.
- **`hl` (str, optional)**: The language code for the search.
- **`next_page_token` (int, optional)**: Token for retrieving the next page of results.
- **`lrad` (float, optional)**: Search radius in kilometers.
- **`uds` (str, optional)**: Filter string provided by Google.
- **`no_cache` (bool, optional)**: Flag to force fresh data retrieval.
- **`aasync` (bool, optional)**: Flag to enable asynchronous search submission.

This function is designed to be flexible and powerful, catering to a wide range of job search scenarios by allowing detailed customization of search parameters.