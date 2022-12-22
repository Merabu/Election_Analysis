# Election_Analysis


## Overview of Election Audit

I am tasked to help Seth and Tom submit the election audit results we have been working on. However, the election commission has requested further editing to provide the vote turnout for each county, the percentage of votes from each county out of the total count, and the county with the highest turnout. The purpose of this election audit anlysis is to find the following results,
overall total number of votes, Identify county with largest voter turnout,Percentage of votes by candidate, Winner total votes, Overall percentage of votes by county
Total number of votes, Winner total vote percentage, and Winning candidate
## Election analysis audit.
### Step 1: Initialize a county list, like the candidate_options list, that will hold the names of the counties.
Initialize a dictionary, like the candidate_votes dictionary, that will hold the county as the key and the votes cast for each county as the values.
county_options = []
county_votes = {}

### Step 2:Initialize an empty string, like winning_candidate,
that will hold the county name for the county with the largest turnout.
Initialize a variable, like the winning_count variable, that will hold the number of votes of the county that had the largest turnout.
largest_county = ""
largest_votes = 0 
 

### Step 3: write a script that gets the county name from each row.
county_name = row [1]
              

### Step 4a:Write a decision statement with a logical operator to check if the county name acquired in Step 3 is in the county list you created in Step 1
if county_name not in county_options:


### Step 4b:If the county is not in the list created in Step 1, add it to the list of county names like you did when adding a candidate to the candidate_options list
county_options.append(county_name)



### Step 4c:Write a script that initializes the county vote to zero, like you did when you began to track the vote counts for the candidates.
  county_votes[county_name] = 0


### Step 5:Write a script that adds a vote to the county’s vote count as you are looping through all the rows, like you did for the candidate’s vote count.
county_votes[county_name] += 1


### Step 6a:Write a repetition statement to get the county from the county dictionary that was created in Step 1.
for county_name in county_votes:

### Step 6b:Initialize a variable to hold the county’s votes as they are retrieved from the county votes dictionary.
votes_county = county_votes.get(county_name)

### Step 6c:Write a script that calculates the county’s votes as a percentage of the total votes.
county_percentage = float(votes_county) / float(total_votes) * 100

### Step 6d:Write a print statement that prints the current county, its percentage of the total votes, and its total votes to the command line.
county_results = (
            f'{county_name}: {county_percentage:.1f}% ({votes_county:,})\n')

### Step 6e: This step will be completed in Deliverable 2.
  print(county_results)    
### Step 6f:Write a decision statement that determines the county with the largest vote count and then adds that county and its vote count to the variables created in step 2
if (votes_county > largest_votes): 
            largest_votes = votes_county
            largest_county = county_name
### Step 7:Write a print statement that prints out the county with the largest turnout.
largest_county_summary = (
        f'\n-------------------------\n'
        f'Largest County Turnout: {largest_county}\n'
        f'-------------------------\n')
    print(largest_county_summary)

## Election Audit Results
The election results shows that the winner is Diana DeGette, winning with 272,892 votes which makes up 73.8% of the the total votes.

![Analysis_results](https://user-images.githubusercontent.com/115379848/209030682-f75e76a5-8f67-4ed4-b356-772089b7998b.JPG)


## Election Audit Summary
In conclusion, The python script is more efficient and effective as compared to excel in this type of vast data. With excel different pivot tables will be needed. The Election Commission can decide to modify the script so that they can have a total number of voters who voted by mail or early voting.

