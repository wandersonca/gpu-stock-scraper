# GPU Stock Scraper

[![PyPI](https://img.shields.io/badge/Python-3.9-green.svg)]()

GPU Stock Scraper is a script to scrape various Canadian computer part supplier websites
and determine if stock exists for a given GPU.

#### Websites ####

At the time of this script, RTX 3080 are being scanned across:
* Newegg.ca
    * Checks online stock
* Bestbuy.ca
    * Differentiates online vs backorder vs nearby-store stock
* Memoryexpress.com
    * Checks online and store stock as one
* Canadacomputers.com
    * Differentiates online vs in-store stock
    * Allows selection of specific stores

#### Instructions ####
1. Download appropriate chromedriver to the local script folder
    1. Can be downloaded from:
        * https://sites.google.com/a/chromium.org/chromedriver/downloads
2. Create a .env file, using .env_sample as a guide, and input email information 
    1. **NOTE**: This method is fairly insecure and Google will ask you to allow insecure apps to use this method
3. Run main.py

Optional steps:
1. Modify search_canada_computers() to reflect your local stores
2. If using Windows, you can uncomment "import winsound" and beep() in scraping_functions.py to get 
a beep sound when stock is detected.
3. If you are receiving an error installing dotenv, try "pip3 install python-dotenv"

#### Next Steps ######
1. Use a more secure method (potentially oauth) for sending emails
2. Further refine search_memory_express() to be store-location specific
3. Refine search_best_buy() to only return matches for select stores
4. Incorporate functioning beep noise for both Linux and Windows when stock is detected.
5. Add pc-canada.com

