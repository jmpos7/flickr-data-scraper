# Flickr Data Scraper
### A Python Data Scraper for Your Photostream

This is a Python script that uses the [Flickr API](https://www.flickr.com/services/api/) to extract data and thumbnail images for all public photos uploaded by a specific Flickr user. The script stores this information in a pandas DataFrame and then writes it to an Excel file.

## Technologies

This script requires the following packages to be installed:
* flickrapi
* pandas
* requests
* Pillow
* openpyxl

## Instructions

1. Clone this repository to your local machine.
2. Install the required packages by running `pip install -r requirements.txt`.
3. Create a `.env` file in the project directory with your [Flickr API key](https://www.flickr.com/services/api/misc.api_keys.html) and secret in the following format:
    ```
    API_KEY = 'your_api_key'
    API_SECRET = 'your_api_secret'
    ```
4. Set the `username` variable in the script to the appropriate value for your Flickr account.
5. Run the script. It will retrieve the photo data and display a message indicating the number of photos that were retrieved.
6. After the photo data is added to the pandas DataFrame, a message will be printed indicating the number of rows of data that were added.
7. The script saves an Excel file in a subdirectory `/data` where the script is located. The Excel file is saved as `flickrdata_YYYYMMDD.xlsx`. If a file with the same name already exists in /data, a number will be added to the end of the filename to avoid overwriting the existing file.

## Notes

* This script is designed to work with Python 3.7 or later.
* To run the script, execute it in a Python environment, such as Jupyter Notebook or Spyder.
* The script will automatically create the `/data` subdirectory if it does not already exist.
* The Flickr API has rate limits that may cause the script to fail if too many requests are made in a short period of time. If this happens, wait a few minutes before attempting to run the script again.

## License

This project is licensed under the MIT License.