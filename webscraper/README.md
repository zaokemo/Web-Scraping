# Steam Discounted Games Scraper

This Python script scrapes information about discounted games from the Steam store and saves the data into an Excel file. The script extracts details like game name, price, discount percentage, and user rating for up to 15 games currently on discount.

## Features
- Fetches game information from the Steam "Specials" section.
- Extracts details: Game Name, Price, Discount Percentage, and Rating.
- Saves the data into an Excel file for further analysis.
- Displays extracted data in the console for quick reference.

## Requirements
To run this script, ensure you have the following Python libraries installed:
- `requests`
- `beautifulsoup4`
- `pandas`

You can install them using pip:
```bash
pip install requests beautifulsoup4 pandas
```

## How to Use
1. Clone or download this script to your local machine.
2. Run the script using Python:
   ```bash
   python steam_scraper.py
   ```
3. If the script runs successfully, it will:
   - Print game details in the terminal.
   - Save the data to an Excel file named `SteamDeals.xlsx` in the current directory.

## Script Behavior
1. Sends a GET request to the Steam store's "Specials" page.
2. Parses the HTML content of the page using BeautifulSoup.
3. Extracts the first 15 games with discounts, gathering the following information:
   - **Game Name**: The title of the game.
   - **Price**: The discounted price.
   - **Discount (%)**: The percentage of discount applied.
   - **Rating**: The game's review summary, if available.
4. Saves the extracted data to an Excel file for further use.

## Output
- **Console Output**: The script displays the extracted game information in a formatted way.
- **Excel File**: An `SteamDeals.xlsx` file is created with the following columns:
  - Game Name
  - Price
  - Discount (%)
  - Rating

## Example Console Output
```plaintext
Game Name: Game Example
Price: $9.99
Discount (%): -50%
Rating: Overwhelmingly Positive (500 reviews)

Data saved to SteamDeals.xlsx
```

## Error Handling
- If the script fails to load the Steam page, it prints an error message with the HTTP status code.
- Missing data fields are handled gracefully with default values like "No Rating".

## Limitations
- The script scrapes a maximum of 15 games.
- It is dependent on the current HTML structure of the Steam store page. If the structure changes, the script might need updates.
- Ensure compliance with Steam's terms of service regarding web scraping.

## End

Feel free to use and modify this script as needed.

