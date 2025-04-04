## Overview
This project translates English dialog datasets into Arabic using Google Translate API. The code processes dialog and summary text pairs, handling special formatting and characters to ensure proper translation.

## Features
- Translates dialog and summary text from English to Arabic
- Handles special formatting markers (#Person1#, #Person2#)
- Preserves line breaks and formatting during translation
- Uses multiple Google Translate service URLs for reliability
- Implements rate limiting and error handling

## Requirements
- Python 3.x
- NumPy
- Pandas
- Datasets library
- py7zr
- googletrans==4.0.0-rc1

## Installation
```bash
pip install numpy pandas datasets py7zr
pip install googletrans==4.0.0-rc1
```

## Usage
1. Place your dialog dataset in CSV format in the input directory
2. Update file paths in the script as needed
3. Run the script to process and translate the data
4. The translated data will be saved as "arabic_dialog.csv" and "arabic_dialog2.csv"

## Processing Details
- The script processes data in batches of 200 records
- Translation is done from English to Arabic
- Special text markers are preserved with proper spacing
- Error handling includes retries and logging of problematic records

## Notes
- Google Translate API has rate limits, so the script includes delays between requests
- Multiple Google Translate service URLs are used to help avoid rate limiting

## Future Improvements
- Add support for more language pairs
- Improve error handling and recovery
- Add progress tracking and reporting
- Optimize batch processing for better performance

## License
[Specify your license here]
