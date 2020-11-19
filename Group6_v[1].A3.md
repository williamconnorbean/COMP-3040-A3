# Manitoba COVID API

## API Description
We offer an API that enables users to track the number of active covid19 cases and the number of death caused by the virus.

## Endpoints
GET: `https://api.manitoba-covid.org/json/cases`

GET: `https://api.manitoba-covid.org/json/deaths`

### Parameters
* date (string): Date provided in the YYYY-MM-DD format. Provides the number of COVID cases in Manitoba on the given date.
* region (string): Manitoba region provided as a string.

## Resources

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
        "active": 1000,
        "recovered": 25000,
        "region": "central manitoba",
        "tests": 300000,
    },
    "status": "OK"
}
```
