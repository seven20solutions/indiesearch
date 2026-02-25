# Indie Search

![Indie Search hero](./screenshot.png)

The independent, open source, search tool you've been looking for.

Indie Search is a "drop in replacement"" for your regular search engine.

It gives you 10 blue links which points to the pages you want. That's it. 

No ads. No products. No tracking (from us anway). No accounts.

## How it works

Indie Search is made to "connect" to a search index provider of your choice. 

Once you're connected, you can personalise the results for your country and you're set to go!

## Two ways to search

You can either "self host" Indie Search (great for desktop users) or use https://indie-search.com/ (best for mobile users).

To start using https://indie-search.com/, get a Serper account. Details below.

To self host, see instructions below.


## Search Index providers
We hope to add more providers in future. Below are the current options.

### Serper Search:
Required to use: https://indie-search.com/    
     
Sign up for a free API and get free credits to start searching today.
 
- No credit card required. 
- Minimal signup information required. 
- Search log can be anonomised for privacy.

Sign up here: https://serper.dev

### Exa.ai Search:
Optional. Only works when self hosting (via localhost).    
    
- Sign up for a free 
- No credit card required

Sign up here: https://dashboard.exa.ai/api-keys

NOTE: We are not affiliated with any providers. 


## Our contribution to the Indie Web

The Indie Web is built on a [handful of principles](https://indieweb.org/principles) which we think will make the web a better place.

The search engine is at the heart of how most people experience the web. 

Indie Search is about give YOU control over your search engine.

We give you the code and the knowledge to host it yourself. You're in control again. 


## Self Hosting

To use all the Search Index providers, you should self host the index.html file. Yes, just the one file.

### How to host it

1. **Run locally** (`python3 -m http.server 8000`, `php -S localhost:8000`, etc.). This gives you access to both providers: the dropdown defaults to Serper Search but you can switch to Exa.ai (labeled “Exa.ai (localhost only)”) and keep each key saved in the UI.

Need more help? 

Ask DuckDuckGo AI: https://duck.ai/chat?ia=chat&duckai=1

## Key Storage

Because the app is entirely static, your API keys and country choice never leave your computer—they are held in `localStorage`. If you are on a shared computer, we don't recommend this as other people can potentially find your API keys.

## All Features

- **BYO key panel**: Enter and save your Exa API key once; the form collapses and keeps a “Change key” toggle for updates.
- **Country selector**: Choose your country and Exa receives it as `userLocation` plus the `numResults` parameter so results align with your locale.
- **Provider switcher**: Serper Search is the default provider and runs everywhere; switch to Exa.ai (labeled “Exa.ai (localhost only)”) whenever you run the app locally so you get full Exa results. Each provider saves its own key so the dropdown stays ready whenever you switch.
- **Retro interface**: A serif “Indie Search” wordmark, centered shell, pastel result cards, blue titles, and green URLs echo the nostalgia of early search engines.
- **Keyboard hotkeys**: `/` focuses search, `Ctrl+K` toggles the key panel, `↑/↓` or `j/k` highlight results, and Enter opens the highlighted link.
- **Theme switcher**: Pick light, dark, or “system” (follows `prefers-color-scheme`) with pill buttons; the selection is saved for future visits.
- **Query permalink**: The `?s=` parameter in the URL mirrors your query so you can bookmark or share searches, and loading such a URL auto-runs the query once a key is stored.

## Make Indie Search your default

1. Run the local server (see above) and keep the page open.
2. In your browser’s search engine settings add a custom engine pointing to `http://localhost:8000/?s=%s` (use `%s` or `{searchTerms}` depending on the browser).
3. Set that custom engine as the default or assign it a shortcut (for example, type `i` + space to fire Indie Search).


Need more help? 

Ask DuckDuckGo AI: https://duck.ai/chat?ia=chat&duckai=1
