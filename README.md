# Starbucks Rewards Program Analysis

## Overview

As a means to attract and retain customers, Starbucks leverages a rewards program that honors regular customers with special offers not available to the standard customer. For this project, we'll be combing through some fabricated customer and offer data provided by Starbucks / Udacity to understand how Starbucks may choose to alter its rewards program to better suit specific customer segments.

While the final report for this project is also stored as PDF in this GitHub repository, you may opt to view the full results also at my personal Medium blog. You can navigate to that using this link: https://medium.com/@dkhundley/starbucks-reward-program-project-cfdad91d4779.

## Datasets and Inputs
For this project, we will be leveraging the data graciously provided to us by Udacity. This is given to us in the form of three JSON files. Before delving into those individual files, let us first understand the three types of offers that Starbucks is looking to potentially send its customers:

- **Buy-One-Get-One (BOGO)**: In this particular offer, a customer is given a reward that enables them to receive an extra, equal product at no cost. The customer must spend a certain threshold in order to make this reward available.
- **Discount**: With this offer, a customer is given a reward that knocks a certain percentage off the original cost of the product they are choosing to purchase, subject to limitations.
- **Informational**: With this final offer, there isn’t necessarily a reward but rather an opportunity for a customer to purchase a certain object given a requisite amount of money. (This might be something like letting customers know that Pumpkin Spice Latte is coming available again toward the beginning of autumn.)

With that understanding established, let’s now look at the three provided JSON files and their respective elements:

**profile.json**
This file contains dummy information about Rewards program users. This will serve as the basis for basic customer information.
(17000 users x 5 fields)
  - gender: (categorical) M, F, O, or null
  - age: (numeric) missing value encoded as 118
  - id: (string / hash)
  - became_member_on: (date) format YYYYMMDD
  - income: (numeric)

**portfolio.json**
This file contains offers sent during a 30-day test period. This will serve as the basis to understand our customers’ purchasing patterns.
(10 offers x 6 fields)
  - reward: (numeric) money awarded for the amount spent
  - channels: (list) web, email, mobile, social
  - difficulty: (numeric) money required to be spent to receive reward
  - duration: (numeric) time for offer to be open, in days
  - offer_type: (string) bogo, discount, informational
  - id: (string / hash)

**transcript.json**
This file contains event log information. Complementing the file above, this file will serve as a more granular look into customer behavior.
(306648 events x 4 fields)
  - person: (string / hash)
  - event: (string) offer received, offer viewed, transaction, offer completed
  - value: (dictionary) different values depending on the event type
  - offer id : (string / hash) not associated with any “transaction”
  - amount: (numeric) money spent in “transaction”
  - reward: (numeric) money gained from “offer completed”
  - time: (numeric) hours after start of test

## Files

The following files attached to this GitHub's repository include the following and for the following reasons:

 - **hundley-starbucks-project.ipynb**: This is the Jupyter Notebook in which I performed all my work, including EDA, data preprocessing, and cluster. The results found in this notebook can also be found in the final report.
 - **hundley-starbucks-final-report.pdf**: This PDF document contains all my final results and analyses as performed in the accompanying Jupyter notebook above.
 - **proposal.pdf**: This document contains the initial project proposal I submitted prior to necessarily beginning this project.
 - **data**: This file contains the three JSON files provided by Starbucks / Udacity as noted above.

## Acknowledgements

Special thanks again to Starbucks and Udacity for providing the data utilized in this project!
