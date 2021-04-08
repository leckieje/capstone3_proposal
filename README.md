# capstone3_proposal


### 1. Supreme Court

This dataset comes from [Oyez](https://www.oyez.org/), "a free law project from Cornell’s Legal Information Institute (LII), Justia, and Chicago-Kent College of Law." The organization has collected audio recordings of oral arguments since 1955, but what I'm interested in is transcripts that accompany the audio. To access the transcripts, I will need to go through the GitHub user below who has aggregated the transcripts into json files. 

The goal of the project would be to do NLP through an LDA process along with topic modeling. Since we have two weeks, I would also try and build a Flask app that could take a topic/keyword as input and return the most relevant transcripts. I'd also be interested in possibly doing some historical analysis to see which topics have come and gone over time and/or which lawyers/firms have been most involved in those topics.

[SCOTUS Transcripts](https://github.com/walkerdb/supreme_court_transcripts/)

---

### 2. Aviation Safety Reporting System (ASRS)

The ASRS database is maintained by NASA and contains narratives of safety information provided by pilots, mechanics, flight attendants, and dispatchers. Some info has been redacted. Here is an example:

ABOUT 2 HRS INTO OUR FLT FROM ZZZ TO ZZZ1, THE R ENG ROLLED BACK SLOWLY AND FLAMED OUT AT FL360. ENG FAILURE RECALL ITEMS AND CHKLIST WERE COMPLETED. WE DECLARED AN EMER, ASKED FOR A LOWER ALT, AND SENT A MESSAGE TO THE DISPATCHER. ONCE IN THE RESTART REGIME, A RESTART WAS ATTEMPTED BUT WAS UNSUCCESSFUL. A DIVERT WAS MADE INTO ZZZ2. AFTER LNDG, THE AIRPLANE WAS EXTERNALLY CHKED BY EMER CREW AFTER WHICH THE AIRPLANE WAS PARKED. I CONTACTED THE DUTY PLT BY PHONE, MADE A LOGBOOK ENTRY, INCLUDED AN ENG FLAMEOUT RPT, AND SECURED THE AIRPLANE.

There is also a shorter synopsis: A B737 EXPERIENCED AN ENGINE FLAMEOUT IN CRUISE FLIGHT. THE FLT CREW DECLARED AN EMERGENCY AND DIVERTED TO THE NEAREST SUITABLE AIRPORT.

The data contains many other features. Most interesting is the aircraft's make/model, but there is also info on flight and light conditions, locations etc. Records go back to at least 1988. I do not have full access to the data yet, but I have email with the database coordinator at NASA should speak with him on the phone in the next few days. 

The goal of the project would also be to uses NLP to do topic modeling, again with LDA (I'm finding I like Bayes want to work more with it). I would hope to link topics with aircraft make/model. If topics are frequently associated with certain aircraft, perhaps an analysis could be done on aircraft safety, highlighting which models typically have which issues. 

[ASRS Database](https://asrs.arc.nasa.gov/search/database.html)

---

### 3. Twitter 2016

I have a data set of 3 million Russian troll tweets from FiveThirtyEight (there are other sources a well including the [Internet Archive] which contains both Russian and Iranian Tweets). I also have a list of Tweet ids around the 2016 election gathered by George Washington University. These Tweets are general to the election and not from Russian/Iran. The entire data set includes 280 million ids, but given limits set by Twitter on downloads, I don't have time to get them all. The tweets are also broken down into subcategories. I would focus on the 'Candidates and key election hashtags' subcategory first. 

The goal would be to identify the troll Russian tweets and separate them from the legitimate tweets. I would use NLP to cluster Tweets by similarity which would hopefully bring out meaningful groupings based on topic/content. I could then analyze the conetent of each group to learn about each of them. The main portion of this project is unsuperrvised, but I could also rate how well I did since I do have labels I could use to compare my results. 

This's project's idea is to use NLP to create vectors from text that can be compared using something like cosine simularity. Documents could then be clustered based on that simularity and then analysis could be done on each cluster, including topic modeling, to identify the issues/concerns/ideas/etc associated with each cluster. 

[Russian Trolls](https://github.com/fivethirtyeight/russian-troll-tweets/)

[GWD 2016 Election Tweet IDs](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/PDI7IN)

---

### 4. Data Privacy

I pitched this dataset last time. As a reminder, the dataset is of data privacy polices at US firms put together by researchers at the Imperial College of London.  It contains 4,078 policies and features for the company name, num paragraphs, num words, fog index, overall index, cookie tracking, and web url. The total word count among the policies is 7,579,947. The shortest document has just 59 words, the longest has 9,791 words, and the mean document length is 1,858 words.  

The goal again would be to use NLP to do topic modeling. I would then want to cluster the policies by topic and analyze the kinds of companies associated with each topic. Do larger, multinational corporations have policies that differ from small startups? I worry some that because all the documents are privacy policies, the topics may be difficult to distinguish or there may not be meaningful differences among them, but maybe I'm wrong there. A stretch goal could be some sort of summarizing of the policies given the topics, but I realize we haven't covered any of those processes.   

[Data Privacy Policies](https://github.com/ansgarw/privacy)

