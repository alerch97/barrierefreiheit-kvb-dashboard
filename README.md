# Dashboard - Monitoring accessibility in Cologne's public transport

An streamlit-based web app for people with a disability to monitor the accessibility of tram stations in Cologne.
The app will include information about current breakdowns of elevators and escaltors. I still have to add the breakdowns of elevators, but everything is already prepared. Furthermore I will add functional elevators and esclators to check if people with a disability can access / leave the tram station.

The code constantly gets live data from an web API and stores them in a database (at the moment SQLite). I get the map via Google Maps API. I speeded up the time refreshing the web app by using streamlits built-in cache mechanisms.

Here you can see a little preview of the web app:

<img width="795" alt="image" src="https://github.com/alerch97/barrierefreiheit-kvb-dashboard/assets/152506794/f7bd3d4b-8855-4486-a252-a644b7a55020">


