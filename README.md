# Arrival-Google-Search

Given a list of names this script will use Google Custom Search API to google the names and output names that has potential to be a VIP. Most things are not implemented yet.

## Background Info

Created to be used along side Infor HMS. This will use a excel file containing names/address/city to determine likelyness of a guest being a VIP.\
Likelyness will be based off the following:\
1. Specific article websites included in search result (Wikipedia, New Yorker, Etc)
2. Has a website that includes their own name.
3. Specific key words in the snippet of a webiste (owner, author, entrepreneur, etc)
4. Social Media page with followers above a ceartain threshold (Follower threshold TBD later)
5. Address/City relates to search results.
6. Looks at email domain if on file. Will automatically flag @graduatehotels, @schultehospitality, @ajcpt, etc.

## Dependencies

API:\
This script will require your own api key and search id from Google. You will need a Google account and activate Google Cloud and set up billing.\
[Google Custom Search API](https://developers.google.com/custom-search/v1/overview)

Libraries:\
[Pandas](https://pandas.pydata.org/) for dataframes and [requests](https://pypi.org/project/requests/) for json results of searches. Use [pip](https://pip.pypa.io/en/stable/) to install.

```bash
pip install pandas requests
```

## Usage

Once you have your API key and Search Engine ID, replace api_key and search_engine_id variable. run find_famous names with the excel file and it will output the raw json file. running the functions below will output a set of names that matched whatever criteria the function looked for.