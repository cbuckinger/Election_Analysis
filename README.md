This commit complies with the command line run requirement of the challenge.  Thanks for etting me know about the problem and thank you for reviewing this 
new submission!

Overview: The purpose of this audit is to certify the election in one of Colorado state’s congressional districts.  Votes are tallied by three different methods, then total votes cast are tabulated by candidate and county to determine the winning candidate and the per-county outcome.  Normally this process is performed in Excel, but the state elections office wants a process which can be automated and applied to other elections as well, including senate and municipal.  The desired outcomes for this project are thus two-fold: to determine the outcome of this individual election; and to create a vote tally process which is flexible and reusable.
Results: 
Total Votes: 369,711
County Votes:
o Jefferson: 10.5% (38,855)
o Denver: 82.8% (306,055)
o Arapahoe: 6.7% (24,801)
* Winner: Denver
* Winning Vote Count: 306,055
* Winning Percentage: 82.8%
Candidate Votes:
* Charles Casper Stockham: 23.0% (85,213)
* Diana DeGette: 73.8% (272,892)
* Raymon Anthony Doane: 3.1% (11,606)
* Winner: Diana DeGette
* Winning Vote Count: 272,892
* Winning Percentage: 73.8%
Recommendations: 
This script can be easily adapted to conclude outcomes for other types of elections.  The reporting script, which details winning by candidate and county, can be altered to report other types of elections. Writing input functions for user-defined parameters which are passed to the main process would give required flexibility.   Such variables would include: a 
* summary title of the election
* date of the election

getting user input and creating flexble code could look like this:
#**************variables
election_title=""
* election_identifier=""
total_votes=0
* 
* issue=[]
* issue_votes{}
* winner=""
* winning_count = 0
* winning_percentage = 0
* 
* #***************user input
* election_title = input ("Election Title :")
* election_date= input("Election Date 'dd/mm/yy' : ")
* day, month, year = election_date.split('/')
* 
* #********************validate date (courtesy www.codevscolor.com/date-valid-check-python#:)
* isValidDate = True
* try:
*     datetime.datetime(int(year), int(month), int(day))
* except ValueError:
*     isValidDate = False
* 
* if(isValidDate):
*     print("Input date is valid ..")
* else:
*     print("Input date is not valid..")
* # Printing type of input value
* 
* #verify variables******************************
* #print ("Election Title", election_title)
* #print ("Election Date", election_date)
* 
* #**************get data file
#****************for yes/no, use dropn# Election_Analysis

Yes/no propositions would be processed separately usin conditional flows.
