# Introduction
In this project, SpaceX Falcon 9 launch dataset is used to pridict the successfull rate of its First Stage being landed.

# Overview
## 01. Data Collection 

### SpaceX REST API
SpaceX REST API is a public API in which allow us access data about launch specifications, rocket used, payload delivered, and landing outcome.

```
https://api.spacexdata.com/v4/
```

We convert the JSON to datafame by using json_normalize function. This makes data as a table 
```
data = pd.json_normalize(response.json()) 
```
### Scraping from Wikipedia
Use Pysone Beautiful Soup package to web scrape HTML tables that contain FAlcon 9 launch records.