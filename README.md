# Wakaru - 分かる - To Understand

## Table of Contents

+ [Introduction](#introduction)
+ [Methodology](#methodology)
+ [Setup](#backend-setup)
+ [Backend](#backend)
+ [Frontend](#frontend)

## Introduction

Curating user experiences has become central to many industries in the digital age, where presenting a unified story, across company and product, is central to a holistic marketing strategy. Customer Service represents one of the pillars of business and controlling a user’s experience in that area is important to presenting a unified front. 

With the emergence of accessible natural language processing technologies, such as IBM’s Watson Tone Analyzer, companies can now track the language and tone of their front-facing employees — such as customer service agents. 

This project is focused on developing methodologies to manage the data received from these natural language processing programs, in such a way as to infer whether front-facing employees are contributing to the story of a business or hurting its overall brand.

Wakaru, the tone analyzer app, aims to present these conclusions to businesses in an easy to understand manner.  

## Methodology

To read a full breakdown of the methodologies used in Wakaru, please refer to the research paper found [here](https://github.com/ACC25/wakaru/blob/master/wakaru_paper.docx).

Wakaru is based on a collection of sample data, taken from anonymous and approved sources, designed to mimic the interactions customers might have with customer service representatives. The raw sample data can be found [here](https://github.com/ACC25/wakaru/tree/master/source_emails). A breakdown of the sample data can be found [here](https://github.com/ACC25/wakaru/blob/master/source_emails/interactions.md).

## Backend Setup

+ Clone the repository `git clone git@github.com:ACC25/wakaru.git`
+ Cd into `wakaru-backend`
+ Run `bundle install`
+ Run `bundle exec figaro install`
+ Create an IBM Bluemix account and get credentials for Tone Analyzer and Natural Language Processing services.
+ Open `config/application.yml` and add your Watson credentials to these environmental variables:
    ```text
    watson_tone_username: ""
    watson_tone_password: ""

    watson_nlp_username: ""
    watson_nlp_password: ""
    ```
+ Run `rake db:seed`
+ Run `rails s`
+ Follow the instructions in frontend setup 

## Frontend Setup

+ Clone the repository `git clone git@github.com:ACC25/wakaru-frontend.git`
+ cd into `wakaru-frontend`
+ Run `npm install`
+ Run `PORT=3030 npm start`
+ Visit `localhost:3030` in your browser, while the backend is still running, and use the following credentials to login:

    ```text
    Username: Wakaru
    Password: password
    ```

## Backend

The backend for Wakaru was built with Rails and can be found [here](https://github.com/ACC25/wakaru-backend). It connects with the frontend using JSON Web Tokens and houses all the logic for email classification. 

## Frontend

The frontend for Wakaru was built with React and can be found [here](https://github.com/ACC25/wakaru-frontend). It connects with the backend using JSON Web Tokens and houses all the logic for displaying email classification data. 
