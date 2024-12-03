# Overall concept

- We must develop this scraper to be non-invasive and make sure that we implement limits to not overload the website of tradingedge.club. Only one server will scrape the data and save it locally, then others can access this database.
- Usage
  - Dashboard main page
  - Positions page
    Check [/wanted-design/wanted-functionality.drawio](/wanted-design/wanted-functionality.drawio) & [/wanted-design/system-design.md](/wanted-design/system-design.md)

# MVP

- posts containing text and images are stored in a local database
- module retrieves these posts
  - filters them: all tickers, list of tickers ['NVDA', 'TSLA']
  - sorts them: by newest

# Final version

- would be great that instead of polling every minute, the server receives new posts notifications and scrapes the posts one by one as they are posted (in order to reduce load on the website)
