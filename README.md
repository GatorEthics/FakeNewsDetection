# FakeNewsDetection
Identify and label Tweets as Fake News

# Table of contents

* [About](#about)
* [Features](#features)
* [Installation](#installation)
* [Run](#run)
* [Development info](#development-info)
* [Reading Material](#reading-material)
* [Ethical discussions](#ethical-discussions)
* [Future work](#future-work)
* [Data used](#data-used)
* [Contact](#contact)

## About

Media outlets and social media platforms run rampant with "fake news," or information that has not been fact-checked, especially as they become more opinionated and stray away from centrist, fact-based reporting. This is an increasing issue in reporting, as the public receives most of their information in this way and depend on these outlets to be informed. According to [BBC](https://www.bbc.co.uk/bitesize/articles/zjykkmn), false information can take many forms (satire, clickbate, propaganda, and mistakes), and it can be classified as disinformation or misinformation. It is very difficult for the public to identify any media outlet or social media post as any of these classifications without reading competing claims or doing their own research. Therefore, the purpose of this project is to show how a potential Fake News Detection tool can be built and used by various platforms to warn users of the content before they read.

This ethical tool will search through Tweets and attempt to label them as "right", "left", "centrist" and also add a level of fake news detection to them. While Twitter is currently working on this feature, it is not completely employed at the moment. The goal of this feature is to minimize the amount of fake news that the public recieves from social media outlets.

This detection is done by searching the selected user's tweets for various words which indicate fake news, such as "most", "least", etc.


The project is funded by Mozilla Foundation and it will be used in Data Analytics course at Allegheny College. Please visit the [Allegheny Ethical CS](https://csethics.allegheny.edu/) for more information.


## Features

- Twitter API to search for a user and their screen name

- Tweet classification(binary)
  - Naive Bayes
  - Linear SVM
  - Credit to Zach Leonardo on [Polarized](https://github.com/leonardoz15/Polarized)
 
 - Tweet classification
    - fake
    - true
    - Credit to @FavioVazquez on [fake-news](https://github.com/FavioVazquez/fake-news)

  

## Installation

- Clone the source code onto your machine

    With HTTPS:

    ```https://github.com/Allegheny-Mozilla-Fellows/FakeNewsDetection.git```

    or With SSH:

    ```git@github.com:Allegheny-Mozilla-Fellows/FakeNewsDetection.git```
    

## Run

After pulling the repo, enter into the src/ directory by using the command `cd src/` and installing the following recommended packages: __tweepy__ and __textblob__ via pip. 

```shell
pip install tweepy
```
and then,

```shell
pip install textblob
```

Please note that you may have to install more packages using pip to run this program (for example, `nltk`, `twitter`, etc.).

After installing these packages, you will run the program with the command
 ```python __main__.py```

After running this command, you will be prompted to enter the name of a given senator, which the API will cross-reference with current Twitter users. You will then confirm the name of the senator and choose your preferred diagram for output. 


## Development info

When under developmnet always install the dependencies with `poetry install` and run the program with `poetry run python program_name`.

You can add new dependencies to `pyproject.toml` either manually or by `poetry add package_name`. Please refer to documentation [here](https://python-poetry.org/docs/cli/#add) for more information.

Use `poetry update` for updating the dependencies to their latest versions as neccessary. Please refer to documentation [here](https://python-poetry.org/docs/cli/#update) for more information.

Please use `pre-commit` hooks for linting the code. Install pre-commit with `pip install pre-commit` or follow the documentation [here](https://pre-commit.com/#install). After cloning the repository locally run `pre-commit install` to install pre-commit into your git hooks.

NOTE: You would have to run `pre-commit install` every time you clone a repository. Please refer to documentation [here](https://pre-commit.com/#usage) for more information.

NOTE: You will not be able to complete commit unless all the linters pass. Only staged changes will be checked at the time of commit.


## Future work

Currently this project examines tweets and users stored in CSV files and it only utilizes the API to cross-reference the user's screen name with what is in the CSV file. Users of this program can experiment within the limitations of these files. This project can be further extended by examining tweets in real-time (i.e., outside of the file/utilizing more that the Twitter API has to offer) and adding more classification algorithims for comparison (i.e., more than just true or false), or adding features to visualize how many tweets contain false information. 

## Reading Material

Here is the list of articles that may give the user more insights into fake news detection.

- [Fake News Detection Algorithims Using Keywords](https://news.mit.edu/2018/mit-csail-machine-learning-system-detects-fake-news-from-source-1004)

- [NLP Fake News Detection is Vulnerable to Attacks](https://arxiv.org/pdf/1901.09657.pdf)

- [Fake News Classification is More Difficult than Identifying it](https://scholar.smu.edu/cgi/viewcontent.cgi?article=1036&context=datasciencereview)

- [Facebook Will Use Fake News Detection](https://www.wired.com/story/facebook-click-gap-news-feed-changes/)

- [Twitter Will Use Fake News Detection](https://www.analyticsvidhya.com/blog/2019/12/detect-fight-neural-fake-news-nlp/)


## Ethical Discussions

- What happens if one news outlet or platform produces more fake news than another? Will that alter the way we percieve news and/or classify facts?

- Why might algorithims be particularly harmful for detecting fake news?

- Should we enforce using fake news detecting algorithims? Do media outlets and social media platforms have an obligation to detect fake news?

- What are some of the ways we can prevent biases in fake news detection algorithims as developers and as users?


## Data used

The files used in this project are retrieved from Zach Leonardo's Polarized project and @FavioVazque's Fake-News project and are stored in `data`. These files store over 95,000 tweets (in `ExtractedTweets.csv` and `ExtractedTweets2.csv` each) and approximately 100 senators (in `senators.csv`). 

The tweets include a senator's party, their Twitter handle, and the content of the tweet. The senators file contains a senator's Twitter username and their party.


## Contact

If you have any questions or concerns about this project please contact:

- Dr. Jumadinova(jjumadinova@allegheny.edu)
- Rachael Harris (harrisr@allegheny.edu)
