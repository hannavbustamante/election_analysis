# Election Analysis - Written Analysis


Overview of Election Audit: Explain the purpose of this election audit analysis.
## Overview of Election Audit
The purpose of this election audit is to provide Tom information about the Colorado congressional analysis. This information includes the total number of votes cast, a complete list of candidates who received votes, total number of votes each candidate received, percentage of votes each candidate won and the winner of the election based on popular vote.

## Election-Audit Results

### How many votes were cast in this congressional election?

369,711 votes were cast in this congressional election.

Screenshot from the terminal after running program:

![Election Results](https://user-images.githubusercontent.com/88729583/132148851-998976f5-0be2-4172-a9ef-5303904b1ae8.PNG)

### Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.

Jefferson: 10.5% (38,855)

Denver: 82.8% (306,055)

Arapahoe: 6.7% (24,801)

Screenshot from the terminal after running program:

![County Votes](https://user-images.githubusercontent.com/88729583/132149064-a0f2ffcd-f5a6-4a6c-8311-2eadc4c738b1.PNG)


### Which county had the largest number of votes?

Denver had the largest number of votes.

Screenshot from the terminal after running program:

![Largest County Turnout](https://user-images.githubusercontent.com/88729583/132149191-0e0d5cab-99ca-409e-85af-2ecd2446b0c0.PNG)


### Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.

Charles Casper Stockham: 23.0% (85,213)

Diana DeGette: 73.8% (272,892)

Raymon Anthony Doane: 3.1% (11,606)

Screenshot from the terminal after running program:

![Candidate Vote Breakdown](https://user-images.githubusercontent.com/88729583/132149385-7a002589-cc66-47b8-896f-d37c9cfb4cf6.PNG)

### Which candidate won the election, what was their vote count, and what was their percentage of the total votes?

Diana DeGette won the election. She received 272,892 votes, 73.8% of the total votes.

Screenshot from the terminal after running program:

![Candidate Vote Breakdown](https://user-images.githubusercontent.com/88729583/132149725-4bcec9eb-df87-4ca8-affb-d920f68083e0.PNG)

## Election-Audit Summary

In a summary statement, provide a business proposal to the election commission on how this script can be used—with some modifications—for any election. Give at least two examples of how this script can be modified to be used for other elections.

Original code:
```
# -*- coding: UTF-8 -*-
"""PyPoll Homework Challenge Solution."""

# Add our dependencies.
import csv
import os

# Add a variable to load a file from a path.
file_to_load = os.path.join("Resources", "election_results.csv")
# Add a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_analysis.txt")

# Initialize a total vote counter.
total_votes = 0

# Candidate Options and candidate votes.
candidate_options = []
candidate_votes = {}

# 1: Create a county list and county votes dictionary.
county_list = []
county_votes = {}


# Track the winning candidate, vote count and percentage
winning_candidate = ""
winning_count = 0
winning_percentage = 0

# 2: Track the largest county and county voter turnout.
largest_county = ""
largest_county_votes = 0


# Read the csv and convert it into a list of dictionaries
with open(file_to_load) as election_data:
    reader = csv.reader(election_data)
```
Modifications -- for any election

``` # -*- coding: UTF-8 -*-
"""PyPoll Homework Challenge Solution."""

# Add our dependencies.
import csv
import os

# Input what file you want to load

file_name = input("What file do you want to load? ")


# Add a variable to load a file from a path.
file_to_load = os.path.join("Resources", file_name)
# Add a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_analysis.txt")

# Initialize a total vote counter.
total_votes = 0

# Candidate Options and candidate votes.
candidate_options = []
candidate_votes = {}

# 1: Create a county list and county votes dictionary.
county_list = []
county_votes = {}


# Track the winning candidate, vote count and percentage
winning_candidate = ""
winning_count = 0
winning_percentage = 0

# 2: Track the largest county and county voter turnout.
largest_county = ""
largest_county_votes = 0


# Read the csv and convert it into a list of dictionaries
with open(file_to_load) as election_data:
    reader = csv.reader(election_data)
```

With this modification, the user can use any election file that is formatted the same way as the election_results.csv file and locted in the "Resources" folder. The program asks the user what file they would like to read from, and the file_to_load variable takes this input. To go even further, I would in the future want to create a way to read a file from any file path, not just files located in the Resources folder.



