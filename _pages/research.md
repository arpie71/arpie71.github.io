---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  
---

{% include base_path %}
## IPE Research 
Two questions motivate my research: First, how and why do domestic and international institutions affect economic performance? Second, what causes institutional change? To explore them, I have focused on both the politics of monetary policy and trade policy. Institutions are important in both types of policy: a more independent central bank should lead to lower inflation but at the same time decreases the economic policy tools a government has at its disposal. Why have some but not all governments agreed to give up discretion over monetary policy; is legal independence enough to guarantee good economic results? Cristina Bodea and I explore these issues in papers published in International Organization and in the Journal of Politics, finding that governments will reform central banks in response to competitive pressures and also that the effects of central banks on outcomes such as inflation or capital inflows is strongest when political institutions such as democracy also restrain politicians from interfering with the central bank. We have also looked at the effect of central bank independence on bond ratings and are currently working on a paper examining the relationship between central bank independence and income inequality.

Trade policy offers another venue to explore the effects of institutions. Trade institutions such as preferential trade agreements have become increasingly common across the world. While it is assumed that they are effective at expanding trade, there is less work exploring why they are effective. For one thing, not all trade agreements are the same. As such, Soo Yeon Kim and I examine what aspects of trade agreements increase trade. We find that agreements that remove more trade policy discretion from a government have a strong effect on trade. In another series of papers, Joanne Gowa and I explore whether trade agreements benefit some members more than others. This work suggests that power politics is important for understanding the design and the effects of trade institutions. 

## Diplomacy
At Columbia, access to the text of a plethora of government documents have extended my research on trade policy in a new direction. In a paper with Matt Connelly, we find that U.S. export promotion in the 1970s by the State Department worked to increase U.S. exports to a country but did not have a corresponding effect on U.S. imports from that country. In a separate paper, we explore whether export promotion works best for allies, for adversaries, or when market barriers are high. We argue that because the State Department played a role in notifying U.S. firms about potential export opportunities and vetting foreign importing firms, it could reduce risks associated with exporting. The State Department could also help U.S. firms with potential trade disputes. Both of these factors should have a larger effect on trade in dissimilar countries than in similar countries. 

The State Department documents also allowed me to explore how much information U.S. officials in Iran had about the Shah's troubles and whether they communicated their knowledge back to policy-makers in Washington D.C. In a paper published in _Intelligence and National Security_, we find that officials in Iran wer keeping D.C. abreast of the events, but the tone of the language did not convey the severity of the threat. 
## Data

To explore these questions, I have developed several original and extensive datasets. Cristina Bodea and I have coded [central bank independence](https://github.com/arpie71/CBIdata) for 144 countries for the years 1970 through 2020. For work with Joanne Gowa, I collected [bilateral trade data](https://github.com/arpie71/interwar) for the first half of the 20th century, relying on national trade publications. We also examined the effect of the Reciprocal Trade Agreements Act on U.S. trade which required gathering [U.S. import data by country at the commodity level for the years 1934 to 1946](https://github.com/arpie71/rtaa).

## Software 

I have also written several software packages for different programs. 

To ease the creation of cross-national data, I wrote a Stata command called ccode. This command translates between different country classification schemes (IMF, World Bank, Banks Cross National Time Series, Correlates of War, and country name) to make it simpler to merge data from different sources. As a followup, I wrote ctyfind that allows users to input a country's name or classification and return other classification schemes for the country. 

Dropbox is often stored in different locations on different computers. To make collaboration easier across users, or even just across computers, I wrote the dropbox command for Stata. This command will look across a user's hard drive to find and move to the Dropbox folder. Version 2 of the command include an `external` option that will start the search on external and secondary drives before moving to the primary drive. Additionaly, I changed the `nocd` option so that the text on the Viewer screen is now clickable and will change to the found Dropbox folder. 

After I moved to Columbia's [History Lab](https://lab.history.columbia.edu), my research focus switched to Natural Language Processing and text analysis. One of my big goals was to run Named Entity Recognition/Named Entity Linking on our collection of more than 5 million documents. To do so I handcoded data to train a spaCy NER model and then created a KnowledgeBase with Wikidata IDs to link the entities found in our documents to their Wikidata ID. For ambiguous entities--those such as Christian Democratic Party or Socialist Party that occur in numerous countries--I set up an algorithm to compare overlapping Wikidata attributes to entities with known Wikidata IDs. For example, a mention of Christian Democrats in a document that also mentions Italy is more likely to refer to the Italian party than to the Chilean one. 

To make our data more searchable, we ran topic modeling on each collection. I set up a pipeline in R to download the text from our MySQL database into R and convert the text into an STM object. The script will then run a searchK function to show model statistics for a range of topics so that users can choose the optimal number of topics. Once the number of topics is chosen, a function will run the topic modeling and output the files History Lab inputs into our database. 

History Lab also has an API to allow access to our data. I wrote packages for both R and for Stata to allow users of either program to make API calls within the program. 
