# Election Audit with Python

## Overview of Project

### Purpose

The purpose of this analysis is to provide additional data of an election audit to an election commission in Colorado. 
We will take a look at creating an automated process with python to report the total number of votes cast, total number of votes for
each candidate, the percentage for each candidate, and the winner of the election based on popular vote.

## Election-Audit Results

- The total number of votes that were cast in this U.S congressional election was 369,711. This was found by having a `total_votes` variable in a for loop where each row in the election dataset is read through. 
  Then the vote value was increased with `total_votes = total_votes + 1` for each row that was read.
  
- I created a dictionary in the for loop where the data file is read, in order to hold the county name and number of votes for each county. Once the values were stored in the dictionary, I used a for loop to go through 
  the dictionary and retrieve the vote count for each county. Then the percentage of total votes for each county was calculated by dividing the vote count of the county over the total votes.
  
- The county that has the largest number of votes was Denver. I created an if statement in the same for loop that goes through the county dictionary to determine the largest turnout. 
  The county vote is stored in the variable `countyVotes` for each county that the loop goes through. Then the county vote is compared to a `county_count` variable that was intialized as zero. If the current `countyVotes` is
  larger than the current `county_count` then the vote number is stored in that `county_count`. The loop goes through all the values to find the largest turnout.

- A for loop was used in order to get the number of votes and percentage of total votes for each candidate. This for loop is similiar to the one used to get the county names and votes except it loops through the candidate dictionary instead.
  There is also an if statement in this for loop as well but this time a condition was used to determine the winning percentage of the candidate.

- The candidate who won the election with the most votes was Diana DeGette. Diana DeGette had a vote count of 272,892 and their percentage of total votes was 73.8%.

![winning_results.PNG](/Resources/winning_results.PNG)

Election Results:

The election results are written to a text file called "election_analysis.txt" by using the write() method.

![election_results.PNG](/Resources/election_results.PNG)

## Election-Audit Summary

This script helps automate the proccess of reporting election results and it can be used for any elections with some modifications. For example, it can be modified to be used in senetorial elections by adding veriables for each party since each state has two senators who are elected.
We can also modify this script to use for local elections by removing the county variable since we are only focusing on one county instead of multiple. 