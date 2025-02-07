# Twitter Dataset and Hydratator

To be discussed April 27th, 2020 & You can add comments, troubles, and useful indications.

## Apply for a Twitter developer account

Otherwise you won't be able to recover the tweets. Here is the link <https://developer.twitter.com/en/apply-for-access>. If you have already a Twitter account it won't take long.

Description of the use of Twitter data for research: <https://developer.twitter.com/en/use-cases/academic-researchers>
Twitter's goal is to: "Learn about public conversation"

Twitter has a useful research toolkit for academic researchers: <https://developer.twitter.com/en/use-cases/academic-researchers/helpful-tools>

## Twitter datasets 

As we discussed, let's all start by familiarizing with a Twitter dataset. Please read, [this blog post](https://covid.dh.miami.edu/2020/04/23/mining-twitter-and-covid-19-datasets/) that I wrote and visit all different datasets to give you an idea of what we will be doing. All four datasets are very interesting, specially these two: 

* [Covid-19 Twitter chatter dataset for scientific use](https://github.com/thepanacealab/covid19_twitter) (Panacea Lab).
   * They start their corpus on January 1st, 2020. 
   * They collect English, Spanish, French
   * They structure the dataset in folders by day, eachone containing a csv file: 
    - 2 version: 1 clean version of tweets (clean-dataset.tsv.gz), and a version with tweets and retweets (dataset.tsv.gz)
    - By using NPL they built a dataset of the 1000 frequent words, bigrams, and trigrams.
   * The problem with this files .tsv is that they are huge, so they are not managable with our laptops.
   
* [COVID-19-TweetIDs](https://github.com/echen102/COVID-19-TweetIDs) (Chen & Ferrara)
  * They start their corpus on January 21th
  * Only in English
  * They structure the dataset in files .txt per hour (year-month-date-hour). 
  * Check their list of [keywords](https://github.com/echen102/COVID-19-TweetIDs/blob/master/keywords.txt)

For now, the best option is to simply make some experiments with one of the .txt file from the Chen & Ferrara dataset. We can choose a day, for example, April 1st, [coronavirus-tweet-id-2020-04-01-00.txt](https://github.com/echen102/COVID-19-TweetIDs/blob/master/2020-04/coronavirus-tweet-id-2020-04-01-00.txt). Download the file or copy and paste the content in a single .txt file. 

## Hydratate 

There are different tools to hydratate tweets, and that the two best known are [Hydratator](https://github.com/DocNow/hydrator) and [Twarc](https://github.com/DocNow/twarc)

We are going to use Hydrator for now because it seems easier and has a GUI. 

Follow the instructions to install it: https://github.com/DocNow/hydrator 

Once is installed, do the follwing: 

- open it, go to "Settings" > "Link Twitter Account"
- your Twitter account will open in the browser 
- click on "Authorize application", and it will give you a pin number. 
- Copy the pin number and paste it in the Hydratator and click Submit PIN. 
- In Hydratator, go to "Add", and select the file with the dataset that you downloaded. 
- Click start... and it will take some minutes

Also, we recommend that you follow the Lesson from the programming historian: Brad Rittenhouse, Ximin Mi, and Courtney Allen, "Beginner's Guide to Twitter Data," The Programming Historian 8 (2019), <https://programminghistorian.org/en/lessons/beginners-guide-to-twitter-data> 

# Twitter dataset metadata

After the "hydratation" is done, we get a csv file with all metadata associated to the tweets. This is the complete list: 
* **`coordinates`**: In Chen & Ferrara dataset it does not appear.
* **`created_at`**:	date
* **`hashtags`**	
* `media`	(if tweet had media attached)
* `urls`	(if tweet had url attached)
* `favorite_count`	
* **`id`**
* `in_reply_to_screen_name`	
* `in_reply_to_status_id`	
* `in_reply_to_user_id`	
* **`lang`**	
* **`place`**:	(exact location)
* `possibly_sensitive`	
* `retweet_count`	
* `reweet_id`	
* `retweet_screen_name`	
* `source`
* **`text`**	
* **`tweet_url`**: link to the tweet itself	
* `user_created_at`		
* `user_screen_name`	
* `user_default_profile_image`	
* `user_description`	
* `user_favourites_count`	
* `user_followers_count`	
* `user_friends_count`	
* `user_listed_count`	
* **`user_location`**
* `user_name`	
* `user_screen_name`	
* `user_statuses_count`	
* `user_time_zone`	
* `user_urls`	
* `user_verified`


# Questions
- Dieyun started drafting a [list of question](https://github.com/dh-miami/narratives_covid19/blob/master/twitter-corpus/questions.md). Let's modify this list begining with simple questions and keep adding more. 
- A preliminary observation--- in the [live sentiment map](https://live.rlamsal.com.np/?__cf_chl_jschl_tk__=56d68a1ec26743f9e124698e38ddeff6b94f3cc4-1588141337-0-ASM3mO67d9FktZw1C0kqm4vBLC6AQPdaDAMWIrxsXHTRIUXoNz_FQ9cAQkOBr6RV2XrqK107UqzV_R9WsIPSBf6fYg4oxAc55rH9Xcc3VcGcrdvb928fRm6AetKR52-k2Y5CwTM9kUx12OMGQ70o1PEujur5xCI4kCt6ynhKpQMMEIgNSH39Eoq2diX5Djl0Ku2LWFetgr41AdLlsPyCdDyi8pU8tJSesewaVvg5PnOlvPX6XSgnlPBDbSn2nbg65bad2_Mp4lfiWW9x_Yhe42Y) while only 22.5% of tweets collected contain negative sentiment, the map shows that tweets with geotags in the Miami area are largely negative. (Dieyun)
- Has anyone been able to download [this](https://ieee-dataport.org/open-access/corona-virus-covid-19-tweets-dataset) data set? I can't find the URL to get the CSV files. (Dieyun)

