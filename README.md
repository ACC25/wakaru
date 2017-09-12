# Wakaru - 分かる - To Understand

## Table of Contents

+ [Introduction](##introduction)
+ [Methodology](##methodology)
+ [Usage](##usage)
+ [Backend](##backend)
+ [Frontend](##frontend)

## Introduction

Curating user experiences has become central to many industries in the digital age, where presenting a unified story, across company and product, is central to a holistic marketing strategy. Customer Service represents one of the pillars of business and controlling a user’s experience in that area is important to presenting a unified front. 

With the emergence of accessible natural language processing technologies, such as IBM’s Watson Tone Analyzer, companies can now track the language and tone of their front-facing employees — such as customer service agents. 

This project is focused on developing methodologies to manage the data received from these natural language processing programs, in such a way as to infer whether front-facing employees are contributing to the story of a business or hurting its overall brand.

Wakaru, the tone analyzer app, aims to present these conclusions to businesses in an easy to understand manner.  

## Methodology

To read a full breakdown of the methodologies used in Wakaru, please refer to the white paper found [here]().

Wakaru is based on a collection of sample data, taken from anonymous and approved sources, designed to mimic the interactions customers might have with customer service representatives. The raw sample data can be found [here](https://github.com/ACC25/wakaru/tree/master/source_emails). A breakdown of the sample data can be found [here](https://github.com/ACC25/wakaru/blob/master/source_emails/interactions.md).

## Usage

## Backend

The backend for Wakaru was built with Rails and can be found [here](https://github.com/ACC25/wakaru-backend). It connects with the frontend using JSON Web Tokens and houses all the logic for email classification. 

## Frontend

The frontend for Wakaru was built with React and can be found [here](https://github.com/ACC25/wakaru-frontend). It connects with the backend using JSON Web Tokens and houses all the logic for displaying email classification data. 
