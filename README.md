# Reddit-Flair-Detection

Classifier to predit the flairs of the post of [r/india](https://www.reddit.com/r/india/)

### Go to [r/india](https://www.reddit.com/r/india/) and open a post

### Copy its url and paste it into the app

Live web app is here:
[Website](https://reddit-heroku-flair.herokuapp.com/)

## Requirements
The following installation has been tested on Ubuntu 18.04.

This project requires **Python 3** and the Python libraries required have been stated in the requirements.txt file.

1. Clone the repo

```bash
git clone https://github.com/gauravchopracg/Reddit-Flair-Detection.git
cd Reddit-Flair-Detection/
```

2. Install Dependencies
```bash
pip install -r requirements.txt
```

## Reddit Data Collection

In this part, I have collected dataset based on:
1. 5 year dataset: from 2015 to  2020 with features title, flair, content, timestamp, comments, nsfw, stickied, and url  on post using PRAW
2. Data set consists of close 250 posts for 12 flairs using praw module.
3. 20 comments per post.
Flairs include Coronavirus,

 
## Exploratoy Data Analysis

In this part, I have tried to analyse the data, build intuition about the data and gain insights from the data. 

## Building a Flair Detector

In this part, I have tried to build the classifier using both baseline ML algorithms and Neural Networks.

## Building a Web Application

Web application has been developed with Python and Flask framework.

**To run the app:**

1. Clone the repo

```bash
$ git clone https://github.com/ashishsalunkhe/Reddit-Flair-Detector.git
$ cd Reddit-Flair-Detector/webapp
```

2. Install Dependencies
```bash
$ pip install -r requirements.txt
```

3. Import the package
```bash
$ export FLASK_APP=rfd.py
```
If you are using Microsoft Windows, use set instead of export in the command above

4. Run
```bash
$ flask run
 * Serving Flask app "rfd"
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
 ```

## Deployment

The web application is deployed to Heroku Cloud platform. 

Can be accessed by querying POST request: 
```
import requests

files = {'upload_file': open('test.txt','rb')}
r = requests.post("https://reddit-heroku-flair.herokuapp.com/automated_testing", files=files)
```

