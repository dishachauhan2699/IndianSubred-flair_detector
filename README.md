# IndianSubred-flair_detector
Designing a model using python to predict the Flair od a post from indian Subredit through it's url.
We didn't use PRAW because of it's 1000 posts limit insted we used
PUSHSHIFT.Io api to for data collection, throught this I  collected around 12000 posts and saved it into a datadic.<br />
and Imported this data into a dataframe.<br />
Intial Flair count for each Flair

|Flair|Count|
|--------|-------|
|'Non-Political'| 2161 |
| 'NaN'| 9838|
 |'Politics'| 2122|
 |'Science/Technology'| 479|
 |'AskIndia'| 1385|
 |'Photography'| 254|
 |'All CAPS.'| 66|
 |'Policy/Economy'| 478|
 |'Business/Finance'| 726|
 |'[R]eddiquette'| 1507|
 |'Sports'| 138|
 |'Food'| 147|
 |'Demonetization'| 80|
 |'Scheduled'| 28,|
 | Low-effort Self Post | 2|
 | Image Rule Violation | 1|
 |Low-effort self-post. | 38|
 | Not Original/Relevant Title | 1|
 | Personal/Unverified Social Media | 1|
 |Post link Directly'| 1|
 | Unverified Content / Disreputed Source |': 5|
 | Self-promotion-Low-effort Self Post | 1|
 Low Quality/Non OC Meme| 3|
 | Not specific to India |': 2|
 | Self-promotion | 1|
 
 Then I removed all rows with flaircount<10 as they won't help and droped soms rows of type NonFlair as there count was too high. Then the
 splitting of data took place into test and train. <br />
 
 Then I saved the data to an instance of Mangodb adn exported it to a json file.
 Then the classification was performed through naivebayes aand LSVM.
