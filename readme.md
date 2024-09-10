
# VK Newsfeed Parser

## Overview
This script is designed to scrape posts from VK's newsfeed based on a specified keyword and date range. It utilizes VK's API to gather data and saves the results in a JSON file.

## Prerequisites
- Python 3.x
- `requests` library

## Setup

1. **Install Dependencies**:
   ```bash
   pip install requests
   ```

2. **Configuration**:
   - Replace `"your_key_word"` with the keyword you want to search for.
   - Replace `"your_access_token"` with your VK API access token.

3. **File Name**:
   - Set `file_name` to your desired JSON output file name.

## Script Workflow

1. **Initial Request**:
   - Performs an initial request to determine the total number of posts available.
   - Calculates the range in hours for fetching posts.

2. **Data Collection**:
   - Scrapes posts based on the calculated date ranges.
   - Extracts relevant post information and appends it to the JSON file.

3. **Pagination**:
   - Manages pagination using the `next_from` parameter to retrieve additional posts if available.
   - Adjusts date ranges to ensure comprehensive data collection.

4. **Completion**:
   - Terminates when no more posts are available or the date range exceeds the initial start date.

## Usage

Run the script using Python:

```bash
python your_script_name.py
```

## Notes
- Ensure your access token has the necessary permissions.
- Adjust the `start_date` and `end_date` to match your desired data collection period.
- The script appends the collected data to the specified JSON file.

