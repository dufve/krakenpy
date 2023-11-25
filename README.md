# KrakenFiles Downloader 🚀

A simple yet efficient Python module that facilitates the downloading of files from KrakenFiles using a given URL.

## Installation

### Prerequisites

Ensure you have Python (3.x or newer) installed. This module also requires `requests`. If not already installed, you can do so via pip:

```bash
pip install requests
```

## Usage  

To use the KrakenFiles Downloader module:

#### 1. Import the module in your Python script:
```
from krakenfiles_module import download_from_krakenfiles
```
#### 2. Specify the KrakenFiles URL:
```
url = "YOUR_KRAKENFILES_URL"
```
#### Optional:
Specify an output directory for downloaded files. If not provided, files will be saved to the current script's directory.
```
output_directory = "YOUR_DESIRED_OUTPUT_DIRECTORY"
```
#### 3. Call the function to download the file:
Very simple example script that utilizes the module:
```
def main():
    # Ask the user for the necessary input
    url = input("Enter the KrakenFiles URL: ").strip()

    # Call the function to download the file
    try:
        filepath = krakenfiles_module.download_from_krakenfiles(url)
        print(f"\nFile successfully downloaded to: {filepath}")
    except Exception as e:
        print(f"An error occurred: {e}")

if __name__ == "__main__":
    main()
```

## Error handling
If there's an issue with obtaining the download link, a ValueError will be raised. It's recommended to handle this error for smoother user experience:
```
try:
    output_path = krakenfiles_module.download_from_krakenfiles(url)
    print(f"File downloaded to: {output_path}")
except ValueError as ve:
    print(f"Error: {ve}")

```
