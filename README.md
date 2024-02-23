# Dashboard - Monitoring accessibility in Cologne's public transport

## Idea
The aim of the project is to record and analyse current failures of lifts and escalators in Cologne's public transport system and present them in a user-friendly dashboard. This will then be made available to the public and contribute to improving the passenger experience for people with physical disabilities. The project is being implemented in Python with the use of Pandas, Streamlit and SQL. The dashboard includes information about current breakdowns of elevators and escaltors. I still have to add the breakdowns of elevators, but everything is already prepared. Furthermore I will add functional elevators and esclators to check if people with a disability can access / leave the tram station.

## Backend
The ETL process runs in the backend, which first accesses the API provided by the KVB and updates the required data in JSON format every 10 minutes. The data received is converted into a Pandas dataframe to calculate the number of breakdowns, installed lifts/escalators and the breakdown rate. In addition, the names of the lifts/escalators including their coordinates are extracted. The relevant data is loaded into an SQL database in order to continuously supplement data already loaded there. Designations and positions are updated in the database after each successful query. Due to the development status, SQLite is used. This ETL process runs regularly in the background as a thread.

## Frontend
The data from the database is transferred to a dashboard as a web app, which is created using the Streamlit framework. The dashboard includes a display of the current failures (live update) as well as dynamic plot of the failure history, which allows the user to adjust the time window using a slider. In addition, an interactive map is added to the dashboard, on which the broken down lifts/escalators are displayed with pin icons. This map integrates the Google Maps API. In a further phase, the dashboard still needs to be converted into object-orientated programming.

Here you can see a preview of the interactive dashboard:

<img width="795" alt="image" src="https://github.com/alerch97/barrierefreiheit-kvb-dashboard/assets/152506794/f7bd3d4b-8855-4486-a252-a644b7a55020">


