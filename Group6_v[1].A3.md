# Manitoba COVID API

## API Description

## Endpoints
GET: `https://api.manitoba-covid.org/json/cases`

GET: `https://api.manitoba-covid.org/json/deaths`

### Parameters
* **date** (string): Date provided in the YYYY-MM-DD format. Provides the number of COVID cases in Manitoba on the given date. If no date is provided the current date is used. 
* **region** (string): Manitoba region provided as a string. If no region is provided "All Manitoba" is used. 

## Resources
```
{
    "cases": number of cases reported on the given date,
    "deaths": number of deaths reported as of the given date,
    "date": date of reported data,
    "active": number of active cases as of the given date,
    "region": region in Manitoba data is filtered on,
    "tests": number of tests performed on the given date
}
```

## Sample request/response
### Request
```
https://api.manitoba-covid.org/json/cases?date=2020-11-19&region=central
```

### Response
```
{
    "results":
    {
        "cases": 150,
        "date": "2020-11-19",
        "active": 1000,
        "region": "central manitoba",
        "tests": 8000
    },
    "status": "OK"
}
```

### Request
```
https://api.manitoba-covid.org/json/deaths
```

### Response
```
{
    "results":
    {
        "deaths": 20,
        "date": "2020-11-19",
        "active": 1000,
        "region": "all manitoba",
        "tests": 8000
    },
    "status": "OK"
}
```
