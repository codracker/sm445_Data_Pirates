# sm445_Data_Pirates
**This repository holds the project under problem statemet SM445 of SIH2020. The problem statement is provided by FIS Global. The project is a corporate action bot.**





[**INTRODUCTION**]


**Team Name-Data_Pirates**


## Contributors to this project are (Team Member - JK Lakshmipat University, Jaipur):
   1. Muskaan Jain- https://github.com/codracker
      EmailID - muskaanjain@jklu.edu.in, Mobile - 8384854406
   2. Harshaditya Gaur- https://github.com/HarshAditya23
      EmailID - harshadityagaur@jklu.edu.in Mobile - 9116190180
   3. Viral Natani- https://github.com/viralnatani
      EmailID - viralnatani@jklu.edu.in, Mobile - 9414834346
   4. Samyak Bhagat- https://github.com/samyak-bhagat
      EmailID - samyakbhagat@jklu.edu.in, Mobile - 7976378845
   5. Vanshika Sharma- https://github.com/sVanshika
      EmailID - vanshikasharma@jklu.edu.in, Mobile - 8890776688
   6. Sanyukta Tanwar- https://github.com/sanyukta0830
      EmailID - sanyuktatanwar@jklu.edu.in, Mobile - 9414177538

## Mentors:
   1. Dr. Amit Sinhal 
      EmailID - amit.sinhal@jklu.edu.in
      Mobile - +919425476655
   2. Mr. Santosh Kumar 
      EmailID - santosh.verma@jklu.edu.in
      Mobile - +919711492804

**Problem Statement**
The Corporate Action Robot is to be developed for retrieving accurate, and complete information on historical, current, and future expected corporate action in timely manner from free sources.Capability of crawling public web pages to retrieve information (Historical,current, future)
Ability of process information available in free text format like pdf, and MS word document 
Extract important information from retrieved pages/files on corporate action



[**RESOURCES**]



## **This project is being built on the following environment:**
    Processor: Intel(R)
    OS: Windows 7,8,10
    IDE: Anaconda Distributions(Jupyter Notebook)
    Language: Python3
    Web Browser: Google Chrome/Mozilla Firefox
    Additional Softwares: MS-Excel, Adobe PDF Reader, Notepad
    Python Language Libraries- Numpy, Pandas, beautifulsoup, urllib, requests
    IDE: Anaconda Distributions(Jupyter)     
    Frontend: Streamlit
    Backend: Spacy
    Database: MySql


	


## **Let us first crawl the workflow of the project:**
      > Web Scraping
      > Data Extraction
      > Text Analytics(PDF)
      > Deploying on UI(Streamlit)
     
     
 ## **References**
      1. https://www.investopedia.com/articles/03/081303.asp
      2.https://www.barclays.co.uk/smart-investor/investments-explained/funds-etfs-and-investment-trusts/corporate-actions-explained/
      3.https://en.wikipedia.org/wiki/Corporate_finance
      4.https://www.referenceforbusiness.com/encyclopedia/Fa-For/Finance.html
      
     
   
   



[**DESIGN**]


  
## **ARCHITECTURE DIAGRAM ** 
  
 ![Architecture](https://github.com/codracker/sm445_Data_Pirates/blob/master/Architecture.jpg)
  

  
## **Web Scraping**
      > Moneycontrol - @https://www.moneycontrol.com/
      > Rediff.com - @https://www.rediff.com/
      > Livemint - @https://www.livemint.com/
      > Screener.in - @https://www.screener.in/
      
   
**To do scrapping following libraries have been used:**

1.Beautiful Soup- Beautiful Soup is a Python library for pulling data out of HTML and XML files
   >pip install beautifulsoup
   
2.urllib- Collects several modules for working with URls- i.e. requests for opening and reading urls
   >pip install urllib

3.requests- Standard for making HTTP requests
  >pip install requests





## **ML MODEL **
   >NLP by Spacy using NER(Name Entity Recognition)with custom entities and annotations[https://github.com/codracker/sm445_Data_Pirates/blob/master/InformationExtraction/NLPmodel.ipynb]




[**Current Progress**]
Data source for corporate actions (CA) 
1.Is it configurable, if yes then what all is configurable?   **Yes**, it is configurable , we are parsing the html code of the website from which we are extracting tabular value , paragraphs(free text) and document links. 

2.Does it support any source, or only specific sources? Name them if specific: It supports multiple sources:-
 > www.moneycontrol.com
 > money.rediff.com/companies/news/Bonus
 > www.screener.in
 > mnacritique.mergersindia.com -->/search/bse?s=bse&category=M-and-A-Digest#

3.Does system support intelligent crawling to identify which all sources can provide data?: No



4.Type of data gathered {Tabular, structured, free text}:
   >Free Text
   >Tabular data (structured data which can be requestb according to the CA)
   >PDF's links of the company announcements 



5.Type of document supported {PDF, MS Word, MS Excel, html, etc.} : PDFlink,html


6.Data collection is scheduled, real time, both: Data collection is on realtime , i.e, whenever the user requests to collect data it will execute and will always get the latest data


7.Technology / tool used: Beautifulsoip,urllib,requests



## **Data Extraction**

1.How is data extracted?: Web crawler outputs continous stream of data (Text strings) which is fed into NLP model.


2.What all datapoints systems can extract from free text?: NLP model: A built-in RNN is trained on Spacy library with custom entities[https://github.com/codracker/sm445_Data_Pirates/blob/master/InformationExtraction/NLPmodel.ipynb].


3.Types of documents successfully processed : This neural net identifies pattern in data, as the position of entity present.System is able to extract key points related to considered corporate actions.

![Architecture](https://github.com/codracker/sm445_Data_Pirates/blob/master/MODEL.jpg)


4.Links of various data that you are able to process, and to what extent (Complete / Partial):





5.Technology / tool used: We were successfully able to extract data from PDF (scanned/typed), using tessaract OCR.





## **Corporate Action scope covered.**
1.CA types supported- Dividends,
                    Could be extended to :Bonus, Splits,AGM/EGM(Board Meetings),Mergers & Acquisitions
                    
                    
2.Financial market supported: No


3.Historical / current: Historical data(extracted from the tabular data of different websites)
		-> Dividend
		->Rights
		->Board meetings
		->AGM/EGM
		->Bonus
		->Split
		->Quater results
		->Profit and loss
		->Balance sheet
		->Cash flows
		->Ratios
		->Share Holding patterns
	
   
   Current data
		Scrapping of Data
			->Free Text(News articles , summary of corporate announcements , Blogs)
			->PDF's links (Documents from company of CA)
			
			

4.Workflow supported:
   i.New announcements of CA: Yes
  
   
  
  
  
 5.Do system compliment / merge data from various sources to make it complete: Yes



## **Quality of data**
We based our reliabilty on making the bot intelligent (Human thought centric).
We are not relying for only one data tuple for every entity related to a Corporate Action. We would be comparing all the 
entries related to an entity and the best one would be select.
The inspiration behind this is A* algorithm and human decision making process.
We would be using 2 heuristics :
1. Source reliable score: Generated purely upon how many times the source was accurate.
2. Information frequency score: How many times an information is repeated.
The cell whith the highest score will be selected for final tuple.
[https://github.com/codracker/sm445_Data_Pirates/blob/master/Reliability.ipynb]


## **Usability**
1.Type of application {Mobile, Web, Desktop}: Deployed on Web
2.Actions user can perform with this system: View information about company' corporate action as well as download the output.
3.GUI for application: Streamlit
4.Input to system and its corresponding output:  Company Selection by user and output regarding company's corporate action/announcements 
5.User overrides / customization possibilities: 
6.Technology / tool used: Streamlit Installation
>pip install streamlit

To run Streamlit
>Type Streamlit run [Filename]


After the successful retrieval and processing of data, the product has to be displayed somewhere. So, the UI(user interface) is built upon the newly developed open-source app framework that is Streamlit[https://www.streamlit.io/]. Various components of streamlit have been taken in use to develop the required UI.

## **Few of the components are:**
    > st.sidebar
    > st.title
    > st.selectbox
    > st.subheader
    > st.button
      
    
 Supporting Libraries with Streamlit-
 
 1. Pandas
 >pip install pandas
 
 2. Numpy
 >pip install numpy



##**Data Management**
1.What is captured by system {Raw input data, Output of extraction tool, Final output}: 
 >Raw input data: Data is  web-scraped
 >Output of extraction tool: Data extracted by SpaCy model
 >Final Output: Structured Information displayed on UI
 
2.How data us stored/Data design? 
  >Data Design
  >Technology / tool used: 



## **Any other features / specialty of system that make it unique**
Yes(UNIQUE), No paid features and data provided is free of cost to the user plus we have provided option to view and download information into portable document format in well structured manner with important and support for information handling, conflicting data and incomplete information.



## ** WOW Factor **
The most amazing part is the reliability. For the reliability two things have been take that is:
 1. Source score
 2. Frequency
 
## ** Performance Stats. **
Efficient retrieval of information from the web via scraper plus data is store in the database, we just need to call the data from there and Machine Learning (NLP) improves itself and learn from data it process and get itself better and more accurate by the time.

## *User Interface*
![UI](https://github.com/codracker/sm445_Data_Pirates/blob/master/sih1.PNG)
![UI](https://github.com/codracker/sm445_Data_Pirates/blob/master/sih2.PNG)
![UI](https://github.com/codracker/sm445_Data_Pirates/blob/master/sih3.PNG)

