# Instagram Comment Analysis Tool

A Python tool for analyzing comments on Instagram posts using Natural Language Processing (NLP) techniques. This tool performs sentiment analysis on entities mentioned in comments and generates a word cloud visualization of comment content.

## Features

- Extracts comments from a specific Instagram post
- Performs entity recognition to identify people, organizations, and locations
- Analyzes sentiment for each identified entity
- Generates a word cloud visualization of comment content
- Exports results to CSV for further analysis

## Prerequisites

```bash
pip install instaloader pandas nltk textblob spacy wordcloud matplotlib
python -m spacy download en_core_web_sm
```

## Required Libraries

- instaloader: For Instagram data extraction
- pandas: For data manipulation
- nltk: For natural language processing
- textblob: For sentiment analysis
- spacy: For entity recognition
- wordcloud: For generating word cloud visualizations
- matplotlib: For displaying visualizations

## Setup

1. Clone this repository
2. Install the required packages
3. Download the spaCy English language model
4. Have valid Instagram credentials ready

## Usage

1. Replace the placeholder credentials in the script:
```python
loader.context.login('Username', 'Password')  # Replace with your Instagram credentials
```

2. Specify the Instagram post URL you want to analyze:
```python
url = 'https://www.instagram.com/p/XXXXXXXX/'  # Replace with your target post URL
```

3. Run the script:
```python
python instagramcomments.py
```

## Output

The script generates two types of output:

1. **CSV File**: 'comments_with_entity_sentiment.csv' containing:
   - Username of commenters
   - Comment text
   - Entity sentiment analysis results

2. **Word Cloud Visualization**: A visual representation of the most common words in comments

## Analysis Details

- Entity Recognition: Identifies PERSON, ORG (Organization), and GPE (Geo-Political Entity)
- Sentiment Categories:
  - Positive: sentiment score > 0
  - Negative: sentiment score < 0
  - Neutral: sentiment score = 0

## Security Note

- Never commit your Instagram credentials to version control
- Consider using environment variables for sensitive information
- The script automatically logs out after completion

## Limitations

- Requires Instagram account with valid credentials
- Subject to Instagram's API rate limits
- Entity recognition is limited to English language

## Contributing

Feel free to fork this repository and submit pull requests for any improvements.

## License

[MIT License](LICENSE)

## Disclaimer

This tool is for educational purposes only. Ensure compliance with Instagram's terms of service and API usage guidelines when using this script.
