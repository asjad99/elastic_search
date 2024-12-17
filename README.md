# Search Service API Documentation

## Repository Overview
This repository provides a robust search service utilizing Elasticsearch and MongoDB, designed for efficient handling of search queries through a web API. It's suitable for developers seeking to integrate advanced search functionalities into their applications.

## Files and Modules

### Python Scripts
- **common.py**: Contains utility functions for logging and JSON operations.
- **config.py**: Defines configuration settings like debug state, default port, and host.
- **create_search_index.py**: Manages the creation and management of search indices in Elasticsearch.
- **search_api.py**: Flask application that processes search API requests.
- **substring_search.py**: Handles substring searches and caching mechanisms.
- **test_client.py**: Command-line client for testing the search API.
- **python_client.py**: A Python client demonstrating how to interact with the API.
- **api_docs.py** and **app.py**: Flask applications serving API documentation.

### HTML Templates
- **base.html**: Base template providing the basic HTML structure.
- **doc.html**: Detailed API documentation accessible via the web.
- **404.html**: Custom page for handling 404 errors.

## Setup and Configuration
Ensure MongoDB and Elasticsearch are configured as per settings in `config.py`. Dependencies should be installed from a `requirements.txt` file (assumed to exist).

## Running the Application
- Start the Flask app (`search_api.py`) to serve the search API.
- Use `test_client.py` or `python_client.py` to interact with the API.
- Access the API documentation through a web browser at the root URL served by `app.py` or `api_docs.py`.

## Documentation and Testing
- API documentation is served via Flask and can be customized in `doc.html`.
- Use the `test_client.py` to send queries to your API and validate responses.

## Deployment Notes
- Adjust `DEBUG`, `DEFAULT_PORT`, and `DEFAULT_HOST` in `config.py` based on your deployment environment.
- Consider adding security layers, such as SSL/TLS, especially for handling production traffic.

## Contribution Guidelines
Encourage contributions through pull requests. Guidelines should include standards for coding, commenting, and testing new features. Issue tracking can be managed via GitHub issues to facilitate community interactions.

## Reusability
This documentation and repository setup is designed to be forked and adapted for any developer looking to implement a search API using Elasticsearch. By following the outlined structure, developers can extend the functionality or integrate it with different databases and frontend frameworks.

