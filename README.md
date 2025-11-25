# Company-Policies-And-Meme-Inflation

This project investigates that introduction of vertical short-video user interfaces (e.g. Instagram Reels) on social media platforms cause lifespan of new meme trends to decrease.

## Motivation

The motivation of the project is to see that whether people consume digital products such as memes faster due to the changes in the methods of consuming those products.These days, we are consuming each physical product faster compared to past whether it is clothes, consumer electronics or foods in our daily lifes. The question whether this reflects the case with cultural products such as music,memes and art came to my mind when me and my friend group couldn't recall what we were laughing at on social media the week before

Instagram and YouTube released their 'Reels' and 'Shorts' sections both in 2020 (Instagram on August 5th and Youtube on September 14th). These dates actually coincide with acquisiton of Musical.ly by ByteDance in order to merge it with Tiktok (2018). This was also a breaking point of the popularity of vertical short-video UI.
https://about.instagram.com/blog/announcements/introducing-instagram-reels-announcement
https://blog.youtube/news-and-events/building-youtube-shorts/ 
https://en.wikipedia.org/wiki/Musical.ly#:~:text=ByteDance%20Ltd.,TikTok%20on%20August%202%2C%202018. 


## Hypothesis

1. Null Hypothesis: The mean of lifespan (trending weeks) of memes emerged before 2020 is the same as the mean lifespan of the memes emerged after 2020
2. Alternative Hypothesis: The mean lifespan of memes emerged before 2020 is longer than that of memes emerged after 2020

## Data Collection

KnowYourMeme.com (KYM) is a website where nearly all of the globally known memes are registered with their background information, origin date and origin platform. Web scraping with request and beautifulsoup libraries was conducted to get a total of 1784 memes starting from the oldest one to the newest one. Even though there were about 44000 memes on the website, a smaller group was created by only picking every 25th meme from the chronological order because 44000 memes would require so much processing power.

The interest data for the memes is gathered via Google Trends python library pytrends. For the memes that emerged prior to 2007 a certain timeframe between 2007-2011 was chosen since it was seen that some of the data was distorted before 2007. For the other memes the analyzed data included the timeframe 4 years starting from the origin date. Of course some of the data was still distored. More explanation is made in data cleaning part of Exploratory_Data_Analysis_and_Hypothesis_Testing.

All these collected data was merged into a single dataframe to be downloaded as a .csv file

Major algorithm and UI changes are posted on the websites of the social media platforms with their dates; therefore, this does not require any special data gathering method.

A meme is considered to be on trends when its interest is higher than the 15% of its peak interest. By doing that all the memes uploaded on the KYM are assumed to be on trends at least one week naturally. However, it makes sense since the website does not include extremely niche categories already. 
