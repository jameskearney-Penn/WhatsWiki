# WhatsWiki ReadMe
## Goal:
The goal of our project is to compile the most news worthy events for each month of 2020 using trending pages on Wikipedia. 
## FilePaths
/Deliverable1/flow diagram : outlines the major components/stages of our project, and how they depend on eachother<br/>
/Deliverable1/MockUps : basic outline of how HIT will be presented to worker and how they input data<br/>
/Aggregation/WhatsWikiAgg : output of scores for user descriptions<br/>
/Aggregation/WikiAggOutput : finalized labels for events based on best scores from user descriptions<br/>
/Aggregation/whatswiki.py : python code for aggregating and outputting what were determined to be best labels<br/>
/Quality_Control/whatWiki_output : output of workers deciding if event is newsworthy or not<br/>
/Quality_Control/whatsWiki : worker descriptions for events they deemed newsworthy<br/>
/Quality_Control/HIT2.html : the html template for our mechnaical turk HIT <br/>
/Raw_Data/RawData : trending wikipedia articles taken from AWS
## Major Components of our Project

### Setting up our data ->
We need to aggregate the wikipedia trending topics data in order to create HITs. In order to do this we will use an online dataset from AWS of Wikipedia trending topics and create a CSV file out of the data. The CSV of trending wikipedia pages will then be inputted into our HITs. (Point Value: 2)

### Build our HITs ->
We need to build our HITs on mechanical Turk and determine the best design in order for Mechanical Turk workers to properly analyze trending topics. The general design of the HIT can be seen in the mockup pdf supplied in the repository. (Point Value: 4)

### Aggregate the results ->
We need to aggregate the data from Mechanical Turk and insure that we received quality. We will do this iteratively through two distinct HITs.  First, we have users select if a term is relevant to trending news based on the csv we supplied taken from Wikipedia.  If a term is deemed relevant, the worker will provide a description for the event.  This task will output the events deemed newsworthy along with their descriptions.  To ensure quality descriptions, we have a second HIT in which workers score the provided descriptions based on their label.  We will use a majority vote to determine "good" descriptions, and output those. (Point Value: 3).

### Display the results ->
We need to build a proper interface in order to display our findings from this project. We will do this by posting an article online displaying our results detailing top trending wikipedia articles. (Point Value: 4)
