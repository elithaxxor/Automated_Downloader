AutoDownloader README

Overview

The AutoDownloader script is a Python program designed to automate the process of downloading files from a list of URLs. It processes a list of websites, parses the download links, and saves the files to a specified directory. This script can handle torrent downloads, archive.org files, and other download repositories, while avoiding certain security measures.

Features

	•	Automatically downloads files from URLs provided in a list.
	•	Supports both torrent and regular file downloads.
	•	Can interact with websites to extract download links using BeautifulSoup.
	•	Organizes downloaded files into specified directories.
	•	Displays useful system and file information before processing downloads.
	•	Includes a dynamic loading spinner during long operations.

Requirements

To run this script, you need the following libraries:

	•	wget
	•	tensorflow
	•	bs4
	•	numpy
	•	pandas
	•	requests
	•	matplotlib
	•	linkGrabber
	•	IPCHECKER (custom module)
	•	__downloadlist (custom module)

You can install the required libraries using the following command:

``` pip install wget tensorflow beautifulsoup4 numpy pandas requests matplotlib linkGrabber

```
Usage: 
	1.	Download Links Preparation:

    ** Prepare a list of download URLs in a file called download_list.txt. The script will use this file to download files in sequence.
	2.	Running the Script:


Execute the script in a Python environment using:
``` python AutoDownloader.py
```

    3.	Follow the on-screen instructions to download files from the provided URLs.


3.	Download Process:``` python AutoDownloader.py```
	•	The program will display system information, the current IP address, and details about the downloads.
	•	It automatically detects torrent and non-torrent links.
	•	Files are downloaded to a folder created in the current working directory.
	4.	Download Status:
The program will output success messages or any errors encountered during the download process.

Key Functions
``` 1. download(to_connect)
    
    This function takes a download URL (to_connect) and downloads the file to a pre-defined location. It handles both torrent files and regular files.
    
   2. torrent_pull(torrentlist)
    
    This function parses a list of potential torrent links and returns the correct magnet link for the file.
    
    3. run_downloader(key)
    
    This function manages the logic of selecting between torrent and file downloads and returns the appropriate links for downloading.
    
    4. bs_req(key)
    
    This function sends an HTTP request to a URL and parses its HTML content using BeautifulSoup to extract the required information.
    
    5. url_req(URL00)
    
    This function handles HTTP requests to a URL with the necessary headers to avoid security blocks, returning the response from the server.
    
    6. display_list()
```

Displays the list of download URLs stored in download_list.txt.

Customization

	•	Modify __downloadlist.py to adjust the list of URLs to be processed.
	•	Modify the directory structure in the script to save downloaded files to the desired locations.


Error Handling

    In case of errors, the script uses Python’s traceback to print detailed error messages and provides hints about the failure.

    License

    This script is open-source and copyrighted by Adel Al-Aali. All rights reserved.

    This README provides a comprehensive overview of the functionality and usage of the AutoDownloader script.
