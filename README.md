# financial-news-dataset

The following dataset contains 51,272 articles scraped from finance.yahoo.com. The articles were published between 2017 and 2023.


## Load the data

The data is in a compressed .xz format. To umcompress the data run the following command:

```bash
xz -d data/*.xz
```

This will restore the original .json files and remove the .xz compressed versions.

## Description of Samples

The json-style sample below provides a description of each of the items in the dataset. Each value is null is the piece of data is unavailable.

| **Key** | **Description** |
|---------|---------------|
| `authors` | List of authors who wrote the article. |
| `date_download` | Timestamp when the article was downloaded in the initial commoncrawl web scrape, in UTC format. |
| `date_modify` | Timestamp when the article was last modified, if available. |
| `date_publish` | Timestamp when the article was originally published, in UTC format. |
| `description` | Short summary of the article. |
| `filename` | Encoded filename that represents the URL of the article. |
| `image_url` | URL of the main image associated with the article. |
| `language` | Language of the article, represented by a two-letter ISO 639-1 code. |
| `localpath` | Local file path where the article is stored, null if not saved locally. |
| `maintext` | Full text content of the article, excluding metadata and formatting. |
| `source_domain` | The domain name of the news source that published the article. |
| `title` | Title of the article. |
| `title_page` | Extracted title from the webpage. |
| `title_rss` | Title extracted from the RSS feed of the source, null if not available. |
| `url` | URL of the original article. |
| `mentioned_companies` | List of stock ticker symbols of companies explicitly mentioned in the article. |
| `related_companies` | List of stock ticker symbols of companies related to one of the mentioned companies by virtue of being in the same industry. |
| `industries` | List of industry codes (HSICCD) associated with the article. |
| `named_entities` | Named entities identified in the article, including persons (PER), organizations (ORG), and locations (LOC). |
| `prev_day_price_{ticker}` | Close price of `<<ticker>>` on the day before publication. |
| `next_day_price_{ticker}` | Close price of `<<ticker>>` on the day after publication. |
| `curr_day_price_{ticker}` | Close price of `<<ticker>>` on the publication day. |
| `sentiment` | Sentiment scores for negative, neutral, and positive sentiment. |
| `emotion` | Emotion analysis with probabilities for different emotions: neutral, surprise, disgust, joy, anger, sadness, and fear. |
| `news_outlet` | Name of the news outlet that published the article. |

## Example:

```
{
        "authors": [],
        "date_download": "2017-03-21 14:38:12+00:00",
        "date_modify": null,
        "date_publish": "2017-03-21 13:42:32",
        "description": "Google has updated its Android and iOS apps to make it easier to find what you want as fast as possible. Google (GOOG, GOOGL) wants to make searching the web on your smartphone a bit easier with new shortcuts for its Android, iOS and web apps. The shortcuts, which will appear just below the search",
        "filename": "http%3A%2F%2Ffinance.yahoo.com%2Fnews%2Fgoogle-search-update-134232625.html.json",
        "image_url": "http://l4.yimg.com/uu/api/res/1.2/sjsi2b_GVrJA37q87B.l4g--/aD02NDk7dz03NDQ7c209MTthcHBpZD15dGFjaHlvbg--/http://media.zenfs.com/en/homerun/feed_manager_auto_publish_494/2bac27673420e5431f59358eae738aea",
        "language": "en",
        "localpath": null,
        "maintext": "Google (GOOG, GOOGL) wants to make searching the web on your smartphone a bit easier with new shortcuts for its Android, iOS and web apps. The shortcuts, which will appear just below the search bar in the Google app, will provide users with quick access to things like the weather, entertainment, places to eat and drink and sporting events in your area.\nThe idea is to make it easier to quickly find information related to movies or sports teams in the news. For instance, if you tap on the Entertainment shortcut, you’ll see tabs for things like recent news, TV shows on tonight and movies playing in theaters. Tap one of those movies and you’ll see reviews, ticket sales and more.\nSo when you plop down on the couch with your significant other you won’t have to have a 10-minute back-and-forth about what’s on tonight. Instead, you can open the app, see what’s on and have a 10-minute back-and-forth about what you should actually watch.\nGoogle says the Eat & Drink tab will provide you with restaurant recommendations based on the time of day and what kind of food you want to cram into your face hole, as well as lists of new places to check out. The Sports tab, meanwhile, gives you a shortcut to news, scores and game times for your favorite teams.\nA lot of these features are already available within the Google app, but you have to do a bit of digging and browsing to get to them. The update makes doing so just a bit easier. It’s also a clear shot at competing apps like Yelp, Fandango and others.\nTo be honest, though, I’m most interested in the smaller shortcuts Google is adding to the app — including a currency calculator, solitaire game, tip calculator, a virtual roll of a die and animal sounds.\nMost people will probably find the tip calculator incredibly helpful, especially when going out to eat in groups. We all know that one person who tries to nickel and dime the server, and this could be a great way to get them to pony up the extra cash for their meal. Or you could just stop inviting them out to eat.\nWhat about that animal sound shortcut? Well, who hasn’t wanted to make a hyper-accurate goat sound in a crowded elevator? No one, that’s who.\nMore from Dan:\nThe 8 features we want in the iPhone 8\nHow to avoid falling for email scams\nNintendo’s Switch breaks launch records, but don’t celebrate yet\nSamsung’s new tablet is a Surface Pro 4 fighter with serious firepower\nHow Google is fighting the war on internet trolls",
        "source_domain": "finance.yahoo.com",
        "title": "Google is making it easier to plan your night in or out",
        "title_page": null,
        "title_rss": null,
        "url": "http://finance.yahoo.com/news/google-search-update-134232625.html",
        "mentioned_companies": [
            "GOOGL"
        ],
        "related_companies": [
            "IGLD",
            ...
        ],
        "industries": [
            7375
        ],
        "named_entities": [
            {
                "entity_group": "ORG",
                "word": "Google",
                "normalized": "GOOGL",
                "company_key": "GOOGL",
                "start": 0,
                "end": 6,
                "score": 0.9920122027397156
            },
            ...
        ],
        "prev_day_price_GOOGL": 848.40002,
        "next_day_price_GOOGL": 829.59003,
        "curr_day_price_GOOGL": 830.46002,
        "sentiment": {
            "negative": 0.0008892515324987471,
            "neutral": 0.3814527094364166,
            "positive": 0.6176580786705017
        },
        "emotion": {
            "neutral": 0.9237646460533142,
            "surprise": 0.04787570610642433,
            "joy": 0.011852817609906197,
            "anger": 0.007247631903737783,
            "disgust": 0.004352721851319075,
            "sadness": 0.003734610741958022,
            "fear": 0.0011718443129211664
        },
        "news_outlet": "finance.yahoo.com"
    },
```

## License

This dataset is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) License, allowing for academic sharing and adaptation while prohibiting commercial use. Researchers may use the dataset under Fair Use/Dealing law, as it is intended for non-commercial research and study, aligning with legal exemptions for academic purposes. By applying this license, we ensure open academic access and maintain compliance with Fair Use/Dealing provisions. Fair Use/Dealing permits the use of copyrighted material for academic purposes because it serves the public interest by enabling research, study, education, and transformative analysis without unfairly impacting the original work's commercial value. 

Fair Use (US Law):

https://www.copyright.gov/fair-use/

Fair Dealing (UK Law):

https://www.gov.uk/guidance/exceptions-to-copyright

## Citation

@misc{drinkall2025financialregression,
      title={When Dimensionality Hurts: Investigating the Role of LLM Embedding Compression for Noisy Regression Tasks}, 
      author={Felix Drinkall and Janet B. Pierrehumbert and Stefan Zohren},
      year={2025},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
}
