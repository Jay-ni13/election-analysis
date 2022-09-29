# Election-Analysis

## Project Overview
The Colorado Board of Elections commission and their liaison have given us the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get the voter turnout for each county.
3. Calculate the percentage of votes from each county out of the total count.
4. Determine the county with the highest voter turnout.
5. Get a complete list of candidates who received votes.
6. Calculate the total number of votes each candidate received.
7. Calculate the percentage of votes each candidate won.
8. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.9.12, Visual Studio Code, 1.71.2

## Results
The analysis of the election shows that:
- There were 369,711 votes cast in the election.
'''

    total_votes = 0
        for row in reader:
            total_votes = total_votes + 1
'''

- The 3 counties participating:
    - Jefferson
    - Denver
    - Arapahoe
- The county voter turnout:
    - Jefferson county cast 10.5% of the vote and 38,855 number of votes.
    - Denver county cast 82.8% of the vote and 306,055 number of votes.
    - Arapahoe county cast 6.7% of the vote and 24,801 number of votes.
- The county with the largest number of votes:
    - Denver, which cast 82.8% of the vote and 306,055 number of votes.
- The 3 running candidates:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
- The candidate results:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.

## Summary
