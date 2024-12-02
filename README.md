# Mini Search Engine for Articles

A simple Node.js application that allows users to add articles, search for articles by keyword or tag, and retrieve article details by ID. The project uses Express.js for routing, Body-Parser to handle JSON requests, and the `fs` module to persist articles in a JSON file (`articles.json`).

## Features

- **Add Articles**: Allows users to add new articles with a title, content, and tags.
- **Search Articles**: Supports searching articles by keyword (in title or content) and/or tag. Results can be sorted by relevance (keyword frequency) or by date.
- **Retrieve Article by ID**: Fetches the details of a specific article using its ID.
- **Persistence**: Articles are stored in memory and also saved in a JSON file (`articles.json`) for persistence.

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository**:
 bash
   git clone https://github.com/YOUR_USERNAME/your-repository-name.git

2. POST /articles
Add a new article.

3. GET /articles/search
Search for articles by keyword or tag.

Query parameters:

keyword: (optional) The keyword to search for in the title or content.
tag: (optional) The tag to filter articles by.
sortBy: (optional, default is relevance) Sort results by relevance or date.
example: GET /articles/search?keyword=node&sortBy=relevance

4. GET /articles/:id
Retrieve an article by its ID.
Example : GET /articles/1

Technologies Used
Node.js: JavaScript runtime for building the server.
Express.js: Web framework for routing and handling HTTP requests.
Body-Parser: Middleware to parse incoming request bodies.
FS (File System): For reading and writing articles to a JSON file.
