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
The analysis of the congressional election shows that:
- There were 369,711 votes cast in the election.
```
    total_votes = 0
        for row in reader:
            total_votes = total_votes + 1
```
- The 3 counties participating:
    - Jefferson
    - Denver
    - Arapahoe
```
    county_name = row[1]
    if county_name not in county_list:
            county_list.append(county_name)
            county_votes[county_name] = 0
        county_votes[county_name] += 1
```
- The county voter turnout:
    - Jefferson county cast 10.5% of the vote and 38,855 number of votes.
    - Denver county cast 82.8% of the vote and 306,055 number of votes.
    - Arapahoe county cast 6.7% of the vote and 24,801 number of votes.
```
    for county_name in county_votes:
        c_votes = county_votes.get(county_name)
        c_vote_percentage = float(c_votes) / float(total_votes) * 100
        county_results = (
            f"{county_name}: {c_vote_percentage:.1f}% ({c_votes:,})\n")
```
- The county with the largest number of votes:
    - Denver, which cast 82.8% of the vote and 306,055 number of votes.
```
    if (c_votes > voter_turnout):
            voter_turnout = c_votes
            largest_county = county_name
```
- The 3 running candidates:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
```
    candidate_name = row[2]
    if candidate_name not in candidate_options:
            candidate_options.append(candidate_name)
            candidate_votes[candidate_name] = 0
        candidate_votes[candidate_name] += 1
```
- The candidate results:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
```
    for candidate_name in candidate_votes:
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")
```
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.
```
    if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage
```

## Summary
