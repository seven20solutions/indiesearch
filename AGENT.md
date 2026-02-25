# Goal

To make a simple Google alternative with an "indie web" vibe.

## How

Using Exa API (https://exa.ai/docs/reference/search-quickstart)

Example:
    
    import Exa from "exa-js";

const exa = new Exa("your-api-key");

const result = await exa.search(
  "blog post about artificial intelligence",
  {
    type: "auto",
    contents: {
      highlights: {
        maxCharacters: 4000
      }
    }
  }
);

## Challenge

This has to be a "static html" application. 

It is a BYO key application. Visiting https://indie-search.statichost.page/ will allow the user to enter their key and run a search query.

They key should be saved to local storage. A note advising this is going to be done and they may wish to understand what that means should be added below the "add your key here" field.

Once the key is saved, you should be able to do this:
    
    https://indie-search.statichost.page/?s=my+search+query
    
This should pull up a search results page with 10 blue links on it, just like Google. I.e. page titles are the blue links, descriptions appear below and the full URL is below that.

A disclaimer that all results are provided by Exa.ai should appear at the bottom.

Try and code this project so that Exa could be switched out for another service should the user decide they like something else.