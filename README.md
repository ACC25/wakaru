# Wakaru - 分かる - To Understand

## Table of Contents

+ [Introduction](#introduction)
+ [Methodology](#methodology)
+ [Backend](#backend)
+ [Frontend](#frontend)
+ [Pictures](#pictures)
+ [Usage](#usage)
+ [Setup](#backend-setup)

## Introduction

Curating user experiences has become central to many industries in the digital age, where presenting a unified story, across company and product, is central to a holistic marketing strategy. Customer Service represents one of the pillars of business and controlling a user’s experience in that area is important to presenting a unified front.

With the emergence of accessible natural language processing technologies, such as IBM’s Watson Tone Analyzer, companies can now track the language and tone of their front-facing employees — such as customer service agents.

This project is focused on developing methodologies to manage the data received from these natural language processing programs, in such a way as to infer whether front-facing employees are contributing to the story of a business or hurting its overall brand.

Wakaru, the tone aggregator app, aims to present these conclusions to businesses in an easy to understand manner.  

## Methodology

To read a full breakdown of the methodologies used in Wakaru, please refer to the research paper found [here](https://github.com/ACC25/wakaru/blob/master/wakaru_paper.docx).

Wakaru is based on a collection of sample data, taken from anonymous and approved sources, designed to mimic the interactions customers might have with customer service representatives. The raw sample data can be found [here](https://github.com/ACC25/wakaru/tree/master/source_emails). A breakdown of the sample data can be found [here](https://github.com/ACC25/wakaru/blob/master/source_emails/interactions.md).

## Backend

The backend for Wakaru was built with Rails and can be found [here](https://github.com/ACC25/wakaru-backend). It connects with the frontend using JSON Web Tokens and houses all the logic for email classification.

## Frontend

The frontend for Wakaru was built with React and can be found [here](https://github.com/ACC25/wakaru-frontend). It connects with the backend using JSON Web Tokens and houses all the logic for displaying email classification data.

## Pictures

## Usage

Wakaru is a proof of concept for classifying emails, and the frontend only supports sending one email response at a time -- for now. The backend can handle much more traffic than the app currently allows. The text area on the homepage is designed to receive a pasted email response for classification.

+ To use the the live application, visit [here](https://wakaru.herokuapp.com), and use the following login credentials:

    ```text
    Username: Wakaru
    Password: password
    ```

+ If you wish to create an account, be aware that the you should set fixtures for several text snippets before expecting any accuracy in the predictions. You can set fixtures by clicking the `good, medium, bad` buttons on the home page before submitting it for classification. In later iterations, new accounts will have access to a default set of data (the same as the public account) to avoid any immediate inaccuracies, but that feature is not yet implemented.

+ If you use the public username, be aware that the anyone can set fixtures and manipulate the results.

The graphs produced when you submit an email response are grouped by category--good, medium, bad--from left to right. Each grouping has three bars for Enjoyment Score (green), Big 5 Score (orange) and Dissatisfaction Score (red). The bars are based on the percentile rank of each score in relation to the category in question. Generally, higher scores mean the email will be categorized in a more positive category. A perfect email for instance, would score in a high percentile rank (90 or above) across all categories and scores. Poor emails will score lower percentile ranks. This means that in the case of the Dissatisfaction Score (red), a higher score is a good thing. All scores were designed to be progressive, in that as you move away from zero it implies positive tonal metrics. The predictions are a summary of the graphical data Wakaru displays. 

## Backend Setup

+ Clone the repository `git clone git@github.com:ACC25/wakaru.git`
+ Cd into `wakaru-backend`
+ Run `bundle install`
+ Run `bundle exec figaro install`
+ Create an IBM Bluemix account and get credentials for the Tone Analyzer and Natural Language Processing services.
+ Open `config/application.yml` and add your Watson credentials to the following environmental variables:

    ```text
    watson_tone_username: ""
    watson_tone_password: ""

    watson_nlp_username: ""
    watson_nlp_password: ""
    ```
+ You will also need to run `rake secret` and copy the output into an environmental variable called `rails_secret_key_base: ""`
+ Run `rake db:seed`
+ Run `rails s`
+ Follow the instructions in frontend setup

## Frontend Setup

+ Clone the repository `git clone git@github.com:ACC25/wakaru-frontend.git`
+ Cd into `wakaru-frontend`
+ Run `npm install`
+ Run `PORT=3030 npm start`
+ Visit `localhost:3030` in your browser, while the backend is still running, and use the following credentials to login:

    ```text
    Username: Wakaru
    Password: password
    ```
