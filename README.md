# Reddit-Flair-Detection

This repo illustrates the how to build a machine learning classifier to predit the flairs of the post of [r/india](https://www.reddit.com/r/india/)

### Go to [r/india](https://www.reddit.com/r/india/) and open a post

### Copy its url and paste it into the app

Live web app is here:
[Website](http://rdflair.herokuapp.com/)

## Requirements
The following installation has been tested on MacOSX 10.13.6 and Ubuntu 16.04.

This project requires **Python 3** and the following Python libraries installed(plus a few other s depending on task):

- [sklearn](http://scikit-learn.com/)
- [Pytorch](http://pytorch.org/)
- [pandas](pandas.pydata.org/)
- [Numpy](http://numpy.org/)
- [Matplotlib](https://matplotlib.org/) 
- [Torchtext](https://torchtext.readthedocs.io/en/latest/data.html)

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

In this part, I have collected two dataset:
1. 1 year dataset: from 2015 to  2020 with features title, flair, content, timestamp, comments, nsfw, stickied, and url  on post using PRAW
2. Balanced dataset: 100 post from 9 flairs using praw module.

 
## Exploratoy Data Analysis

In this part, we have try to analyse the data, build intuition about the data and gain insights from the data. 

## Building a Flair Detector


## Building a Web Application

Web application has been developed with Python and Flask framework. The project has been developed using the tutorial [Flask Mega-Tutorial for Python 3.6](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)

**To run the app in you computer:**

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

The web application is deployed to Heroku cloud platform. A developer API using flask has been implemented, which returns a JSON containing a python dictionary in which key is URL of post and values are predicted flair. 

Can be accessed by querying POST request: 
```
import requests

files = {'upload_file': open('test.txt','rb')}
r = requests.post("http://rdflair.herokuapp.com/automated_testing", files=files)
```

