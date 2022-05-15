# SHARE: Designing Multiple Criteria-Based Personalized Research Paper Recommendation System
	


Feature Extraction-
1.	Take query from the user
2.	Input the query to Google scholar; Scrape all Research Papers available in PDF format in the first 3 pages of results.
3.	Extract all text data from the pdf and extract various features like keywords, Citation data from it.
4.	Extract KDM, SCA, SQM, CAOTvalues for each paper from the data extracted.
5.	Use trained LDA + Word2vec model to get the topic number of each scraped paper.


New User Recommendation:
1.	Apply MCDA on the extracted features of the scraped papers to get Utility value of each paper.
2.	Use the Flask application to display the Top Papers sorted according to their Utility Value.
3.	When user clicks on a paper to read it, that information is taken and stored in Database.

Old User Recommendation:	
1.	Query and extract all previous papers read by the user from Database.
2.	Apply LSTM model to get the next Topic preference of the user.
3.	Filter papers according to the Topic preference obtained in LSTM model 
4.	Use combined method of MCDA and SVM to get utility value of each paper and sort them to display in the web application,
5.	When user clicks on a paper to read it, that information is taken and stored in Database.


Requirements

Python 3.6
SQL Lite
To run the program execute app.py

File description

Flask Python app : deatails about GUI
Log: output log of the recommendation system
Requirements: Details about package with version used in this system
Untitled: main program
Data: eaxmple data
User_Deatils: User profile description

