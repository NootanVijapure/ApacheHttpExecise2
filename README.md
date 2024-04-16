### Trending GitHub Repositories Program Guidelines

#### Objective:

To create a Java application that fetches and displays data about trending GitHub repositories for a specified programming language.

#### Requirements:

1.  **Apache HttpClient:** Use Apache HttpClient to send HTTP GET requests to the GitHub API.
    
2.  **JSON Parsing:** Parse the JSON response from the GitHub API to extract relevant repository information.
    
3.  **User Input:** Allow the user to specify the programming language for which they want to fetch trending repositories.
    
4.  **Error Handling:** Implement error handling to handle cases such as invalid user input, network errors, or API response errors.
    
5.  **Structured Output:** Display the extracted information about trending repositories in a structured and readable format.
6.  **Url should be  something like this:** String apiUrl = "https://api.github.com/search/repositories?q=language:" + language + "&sort=stars&order=desc";

    

#### Guidelines:

1.  **Project Setup:**
    
        
    *   Add the Apache HttpClient library and JSON library (e.g., org.json) to your project dependencies.
        
2.  **HTTP Request:**
    
    *   Construct the GitHub API endpoint URL based on the user's input for the programming language.
        
    *   Create an instance of HttpClient and HttpGet to send an HTTP GET request to the GitHub API endpoint.
        
3.  **Handling the Response:**
    
    *   Extract the JSON response body from the HTTP response using EntityUtils.
        
    *   Parse the JSON response using the JSON library to convert it into a JSONObject or JSONArray.
        
4.  **Data Extraction:**
    
    *   Iterate over the JSON array of repository objects to extract relevant information for each repository.
        
    *   Extract fields such as repository name, description, stars count, forks count, and URL.
        
5.  **Display Output:**
    
    *   Display the extracted information about trending repositories to the user in a structured format.
        
    *   Print each repository's details, including name, description, stars, forks, and URL.
        
6.  **Error Handling:**
    
    *   Implement error handling to catch and handle exceptions that may occur during HTTP request execution, JSON parsing, or data extraction.
        
    *   Display informative error messages to the user to indicate any issues encountered.
        
7.  **Resource Management:**
    
    *   Ensure proper resource management by closing the HttpClient instance after use to release system resources.
