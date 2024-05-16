News API is a service that provides last news from API calls.

We will see how to authenticate directly with query parameters.


### 1- Let’s consider this url: https://newsapi.org/v2/everything?q=tesla&sortBy=publishedAt&apiKey=API_KEY

What are the scheme, the host, the path and the query parameters?
+ scheme : https
+ the host : newsapi.org
+ the path : /v2/everything


### 2- Use Insomnia and perform a GET request on this same url.

What status code do you get? Can you understand the error from the content returned?
+ Error 401
+ I need to set an API KEY instead of API_KEY

### 3- The service needs us to be authenticated. Why?

+ Because of the limit of request per day

### 4- Create an account and get your API key.
Replace the query parameter value API_KEY with the one created and execute the query.

+ What is the status code? 200
+ Can you read some articles? Yes

Troubleshoot

### 5- Let's say that we only want the results with French headtitles. How do we do this?

+ By adding a query parameter : language = fr

6- Looking at the documentation, are all results returned?
Which query parameter allows you to define the number of results? The page you want?
+ PageSize = 100 by default
+ Page = 1
