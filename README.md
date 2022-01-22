# Election Analysis

## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.63.2

## Summary
The analysis of the election shows that:

- There were 369,711 votes cast in the elction.
- The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
- The candidate results were:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.

## Challenge Overview
For this project's challenge we were asked to do additional analysis to complete the audit. Specifically, we are to examine the number of votes by county.

1. Calculate the voter turnout for each county.
2. Calculate the percentage of votes for each county out of the total count.
3. Identify the county with the highest turnout.

## Challenge Results
The analysis by county show that:

- The following counties registered votes in this election:
    - Jefferson
    - Denver
    - Arapahoe
- The number of votes by county were:
    - Jefferson county had 10.5% of the total votes and 38,855 number of votes.
    - Denver county had 82.8% of the total votes and 306,055 number of votes.
    - Denver county had 6.7% of the total votes and 24,801 number of votes.
- The county with the highest turnout was:
    - Denver county, who had 82.8% of the total votes and 306,055 number of votes.

## Challenge Summary
While this analysis focused on one specific congressional election in Colorado, we can quite easily adjust the code to peform analysis on any election that has similiar inputs or characteristics. To adjust the script for another election you will have to make the following adjustments:
1. The Python code looks for an election_results.csv file with three specific columns. You have two options for running the script against a different set of results.
    - You may change the content of election results file located here: [Election Results](https://github.com/haldud/election-analysis/blob/ae04fa5a484747b61e53b7a6fe740719d6d32143/Resources/election_results.csv)
    - You may adjust the following line of code to point to a completely different election results file:
    
      ``` file_to_load = os.path.join("Resources", "election_results.csv") ```  
2. Similarily, you may also adjust the result file to write to a different location by adjusting the following code:
    
      ``` file_to_save = os.path.join("analysis", "election_results.txt") ```  
      

The code currently assumes that the data is county based and that the results format is a CSV file with three columns:
1. The first columnn in the CSV file is the Ballot ID. This column is ignored in the program, but it is important to note that the lines in the CSV files represent unique ballots in the election.
2. The second column is the County. With a few changes in the code we could support the analysis or auditing for any types of jurisdiction, such as states or cities.
3. The third column is the selected Candidate on the ballot.
