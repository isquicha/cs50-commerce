# Commerce
## Description
CS50’s [Web Programming with Python and JavaScript](https://cs50.harvard.edu/web/2020/) Project 2 - [Commerce](https://cs50.harvard.edu/web/2020/projects/2/commerce)

## Project description
Design an eBay-like e-commerce auction site that will allow users to post auction listings, place bids on listings, comment on those listings, and add listings to a “watchlist.”

## How to run
[Python3](https://www.python.org/) is a requirement.  
- `git clone` this repository or download and extract .zip
- Open terminal in project folder
  - (Optional) Create and activate a Python virtual environment
    - Windows: `python -m venv .venv && .venv\Scripts\activate.bat`
    - Linux: `python3 -m venv .venv && source .venv/bin/activate`
- Install requirements with `pip install -r requirements.txt`
- Run with `python manage.py runserver` or `python3 manage.py runserver`

## TODO
- [X] Entry Page: Visiting /wiki/TITLE, where TITLE is the title of an encyclopedia entry, should render a page that displays the contents of that encyclopedia entry.
  - [X] The view should get the content of the encyclopedia entry by calling the appropriate util function.
  - [X] If an entry is requested that does not exist, the user should be presented with an error page indicating that their requested page was not found.
  - [X] If the entry does exist, the user should be presented with a page that displays the content of the entry. The title of the page should include the name of the entry.
- [X] Index Page: Update index.html such that, instead of merely listing the names of all pages in the encyclopedia, user can click on any entry name to be taken directly to that entry page.
- [X] Search: Allow the user to type a query into the search box in the sidebar to search for an encyclopedia entry.
  - [X] If the query matches the name of an encyclopedia entry, the user should be redirected to that entry’s page.
  - [X] If the query does not match the name of an encyclopedia entry, the user should instead be taken to a search results page that displays a list of all encyclopedia entries that have the query as a substring. For example, if the search query were Py, then Python should appear in the search results.
  - [X] Clicking on any of the entry names on the search results page should take the user to that entry’s page.
- [ ] New Page: Clicking “Create New Page” in the sidebar should take the user to a page where they can create a new encyclopedia entry.
  - [ ] Users should be able to enter a title for the page and, in a textarea, should be able to enter the Markdown content for the page.
  - [ ] Users should be able to click a button to save their new page.
  - [ ] When the page is saved, if an encyclopedia entry already exists with the provided title, the user should be presented with an error message.
  - [ ] Otherwise, the encyclopedia entry should be saved to disk, and the user should be taken to the new entry’s page.
- [ ] Edit Page: On each entry page, the user should be able to click a link to be taken to a page where the user can edit that entry’s Markdown content in a textarea.
  - [ ] The textarea should be pre-populated with the existing Markdown content of the page. (i.e., the existing content should be the initial value of the textarea).
  - [ ] The user should be able to click a button to save the changes made to the entry. Once the entry is saved, the user should be redirected back to that entry’s page.
- [ ] Random Page: Clicking “Random Page” in the sidebar should take user to a random encyclopedia entry.
- [X] Markdown to HTML Conversion: On each entry’s page, any Markdown content in the entry file should be converted to HTML before being displayed to the user. You may use the python-markdown2 package to perform this conversion, installable via pip3 install markdown2.
  - [ ] Challenge for those more comfortable: If you’re feeling more comfortable, try implementing the Markdown to HTML conversion without using any external libraries, supporting headings, boldface text, unordered lists, links, and paragraphs. You may find using regular expressions in Python helpful.
  
- [ ] Models: Your application should have at least three models in addition to the User model: one for auction listings, one for bids, and one for comments made on auction listings. It’s up to you to decide what fields each model should have, and what the types of those fields should be. You may have additional models if you would like.
- [ ] Create Listing: Users should be able to visit a page to create a new listing. They should be able to specify a title for the listing, a text-based description, and what the starting bid should be. Users should also optionally be able to provide a URL for an image for the listing and/or a category (e.g. Fashion, Toys, Electronics, Home, etc.).
- [ ] Active Listings Page: The default route of your web application should let users view all of the currently active auction listings. For each active listing, this page should display (at minimum) the title, description, current price, and photo (if one exists for the listing).
- [ ] Listing Page: Clicking on a listing should take users to a page specific to that listing. On that page, users should be able to view all details about the listing, including the current price for the listing.
  - [ ] If the user is signed in, the user should be able to add the item to their “Watchlist.” If the item is already on the watchlist, the user should be able to remove it.
  - [ ] If the user is signed in, the user should be able to bid on the item. The bid must be at least as large as the starting bid, and must be greater than any other bids that have been placed (if any). If the bid doesn’t meet those criteria, the user should be presented with an error.
  - [ ] If the user is signed in and is the one who created the listing, the user should have the ability to “close” the auction from this page, which makes the highest bidder the winner of the auction and makes the listing no longer active.
  - [ ] If a user is signed in on a closed listing page, and the user has won that auction, the page should say so.
  - [ ] Users who are signed in should be able to add comments to the listing page. The listing page should display all comments that have been made on the listing.
- [ ] Watchlist: Users who are signed in should be able to visit a Watchlist page, which should display all of the listings that a user has added to their watchlist. Clicking on any of those listings should take the user to that listing’s page.
- [ ] Categories: Users should be able to visit a page that displays a list of all listing categories. Clicking on the name of any category should take the user to a page that displays all of the active listings in that category.
- [ ] Django Admin Interface: Via the Django admin interface, a site administrator should be able to view, add, edit, and delete any listings, comments, and bids made on the site.

