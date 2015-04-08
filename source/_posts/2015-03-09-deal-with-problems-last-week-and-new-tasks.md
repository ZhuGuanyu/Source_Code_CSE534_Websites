---
layout: post
title: "Deal with problems last week and New tasks"
date: 2015-03-09 13:36:39 -0500
author: Guanyu Zhu
comments: true
categories: meeting
---

### What we have done:   

* Combinated the same threads(original posts and reply posts)  
* We used python to remove the punctations and some unrelated words(stopwords). The origal stopwords what we are using is <a href="http://zhuguanyu.github.io/fundamental_of_network/documents/stop_words_en.txt" style="color:blue">here</a>. 

### Problems and New tasks:

The stopwords are not enough. We should also remove the people names, places names, etc. So we summary the unrelated words to the following 9 categories.     

 1. Spurious data.           
 2. Links. Then we ignored the url, website links and email links in the posts.         
 3. Punctuations and Numbers.      
 <!-- more -->     
 4. Traceroute measurements.        
 5. Stop words. We use a list of stop words obtained from the SMART information retrieval system.         
 6. Organization and Human names.         
 7. Time-related and Place-related words. Such as day, night, NYC, San Jose, etc.    
 8. Some unrelated abbreviation words. Such like ICS, ISP, etc.       
 9. Others. This includes some entities words( like issue,information, etc) or phrase(like in order to)    
  