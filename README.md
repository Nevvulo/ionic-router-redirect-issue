# ionic-router-redirect-issue
A minimal reproducible example repository demonstrating an issue with parameters being inaccessible after using `<Redirect />` in a fallback route

## Reproduction
To reproduce the problem:
1) Navigate to localhost:8100 (or the test app) in a new tab. 
    This should load tab 2.
2) Click on "Tab 1".
    This should take you to `/tab1/TESTING`.
    
3) The page should read **"Tab 1 with param: undefined"** when it should actually say **"Tab 1 with param: TESTING"**. 

The console will also print empty objects: this is the `match.params` object. 

You should notice that reloading the page will print the correct parameter data.
