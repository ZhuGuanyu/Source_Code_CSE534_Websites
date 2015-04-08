---
layout: post
title: "Add tf-idf function module and using NLTK"
date: 2015-03-24 13:17:10 -0400
comments: true
categories: meeting 
---

This week we add tf-idf function module and using NLTK to help us lemmatize the text. 

The following is the function that lemmatizate the text.   
{% codeblock Lemmatizations function lang:python %}
def tokenize(text):
    text = ' '.join(text)
    tokens = nltk.tokenize.TreebankWordTokenizer().tokenize(text)
    #print tokens
    # lemmatize words. try both noun and verb lemmatizations
    lmtzr = WordNetLemmatizer()
    for i in range(0,len(tokens)):
        #tokens[i] = tokens[i].strip("'")
            res = lmtzr.lemmatize(tokens[i])
            if res == tokens[i]:
                tokens[i] = lmtzr.lemmatize(tokens[i], 'v')
            else:
                tokens[i] = res
    
    # don't return any single letters
    tokens = [t for t in tokens if len(t) > 1 and not t.isdigit()]
    return tokens
{% endcodeblock %}

We also use the <a href="http://www.nltk.org/nltk_data/" style="color:blue">NLTK DATA</a> help us to deal with the text analysis. 
Here are the English names(<a href="http://zhuguanyu.github.io/fundamental_of_network/documents/male.txt" style="color:blue">male</a> and <a href="http://zhuguanyu.github.io/fundamental_of_network/documents/female.txt" style="color:blue">female</a>) provided by NLTK Data. 
