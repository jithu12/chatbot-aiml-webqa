# Intelligent conversation model

## Overview
AIML artificial intelligence markup language
2. WebQA Open Domain Q & A
3. Deeplearning
Effect display

![alt text](docs/1.png "title")

![alt text](docs/2.png "title")

## Start the service
### Environmental Notes
Linux / Python2.7 / PyCharm

### Install dependencies
```
$ pip2 install jieba
$ pip2 install aiml
$ pip2 install lxml
$ pip2 install beautifulsoup4
$ pip2 install flask
```


### Running process
Working directory: chatbot-aiml-webqa/core
```
$ cd chatbot-aiml-webqa/core
$ python2 web/server.py (or $ nohub python2 web/server.py)

> ......
> * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)

CURL:
$ curl "0.0.0.0:5000/chat" -d "message=新闻"
$ curl "0.0.0.0:5000/chat" -d "message=天气"
$ curl "0.0.0.0:5000/chat" -d "message=时间"
```

## Processing process
### Step 1: Preprocessing
Limit the number of words
2. Filter sensitive words (nausea, politics, pornography, illegal ...)

### Step 2: Knowledge Base Matching (AIML)
1. Basic functions: hello, chat ...
2. Exception Handling: The question is too long, blank question, no reply found ...
3. Emotional answers: expressions, compliments, mocking ...

If no answer is found, go to step 3.

### Step 3: Internet Search (WebQA)
1. News ---- Sina News
2. Articles-Daily Article
3. Joke ---- Encyclopedia of Funeral Affairs
4. Time-Sogou time
5. Weather ---- Sogou Weather
6. Air ---- Sogou Air
7. Other Traversing Baidu Search
> * Baidu Chinese
> * Baidu translation
> * Baidu Atlas
> * Baidu exchange rate
> * Baidu Computing
> * Baidu Stock
> * Baidu Lyrics
> * Baidu latest
> * Baidu Encyclopedia
> * Baidu know

If no answer is found, go to step four

### Step 4: Neural Network
The next-generation dialogue engine based on the Seq2Seq model is not only to train the best answer among existing answers, but to be able to self-create a human-like answer.
Corpus: http://61.93.89.94/Noah_NRM_Data/
There is currently no time to implement this part ... temporarily use Turing Robot API instead ~~~

### Learning function
Use AIML template + shelve storage
1. \ * Wrong *
2. \ * Wrong answer *
3. ......
`` `
ME> Who is the prettiest person in the world
AI> Cinderella
ME> you are wrong
AI> Then teach me
ME> Snow White
AI> I learned, next time you can ask me "Who is the most beautiful person in the world" ...
ME> Who is the prettiest person in the world
AI> Snow White
`` `

## Reference link
1. https://github.com/SnakeHacker/QA-Snake
2. https://github.com/ictar/XIXI
3. https://github.com/fwwdn/sensitive-stop-words
