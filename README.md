# Spring Cloud Gateway Example

This is an example of how to use Spring Cloud Gateway 😃

## What concepts were used in this example?

- I used https://httpbin.org as an example of uri I want to route my request to. So, when I run the application and make a request to localhost:8080, I want this uri to be reached.
- Then, I used two predicates:
  - Path=/hello - When I make a request to /hello, this predicate will be true.
  - Method=GET - When I make a GET request, this predicate will be true.

Therefore, whenever both predicates are true, the redirect will be made to the specified uri.

Then, I used one filter:
  - SetPath=/get
    
Which basically means that when I make a request to localhost:8080/hello?Hello=Cissa, the /hello will be replaced by /get, thus making the request to the uri work correctly.
