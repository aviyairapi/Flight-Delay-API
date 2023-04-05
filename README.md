# Flight-Delay-API
Real-time flight delay data for airports and airlines globally.

<div id="header" align="center">
  <img src="https://media.giphy.com/media/LRZc4dV2kf787nbOB3/giphy.gif" width="100"/>
</div>

[Aviyair’s Flight Delay API](https://aviyair.com/flight-delay-api/) provides real-time delay and cancellation data. This way, you can find out about and track if a passenger or cargo flight is delayed or canceled for any reason. Tracking delay and cancellation status in real-time are essential to provide real-time airport and travel services efficiently, so the global data of Aviyair will allow you to provide data-driven solutions for all markets, whether local or global.

The flight delay data is accessible via GET requests and data is returned in JSON format. Other formats may be added in the future. Let us know if you have a demand for a specific format!

The API provides real-time flight delay data with static information such as the flight number, airline, departure and arrival airports etc. as well as updated, real-time data such as flight status, total delay in minutes, scheduled/estimated/actual departure and arrival times, gate, terminal and more. 

Get complete airport flight delay data in a single call or narrow down the data to flights of a certain airline, flight number, status and others.

--------

## Main Endpoint and Filters with Description

**GET** ` https://aviyair.com/api/v1/flightdelay?key=[API-KEY]&airport_iata=IST&type=departure`

Airport IATA code and schedule type (can be either departure or arrival) are obligatory fields. You can add the below filters to narrow down the flights within the schedule.

| Request Parameter  | Description |
| ------------- | ------------- |
| airport_iata  | Filter the flights based on the three-letter IATA code for arrival airport  |
| type  | Filter the flights based on the aircraft status as either depature or arrival   |
| status  | Filter the flights based on the flight status designated as (started, en-route, landed, unknown) For outputs limit the value  |
| departure_iata  | Filter the flights based on the three-letter IATA code of the departure airport  |
| departure_icao | The ICAO code for departure airport |
| departure_terminal | Departure flight's terminal |
| departure_delay  | Departure delay measured in minutes  |
| departure_sch_time  | Scheduled departure of flight  |
| departure_est_time | Estimated time of departure of the fligth  |
| departure_act_time  | The actual time of departure of the flight |
| departure_est_runway  | Estimated time of departure at runway  |
| departure_act_runway | The actual time of departure at runway |
| arrival_iata | The IATA code of arrival airport  |
| arrival_icao | The ICAO code for arrival airport  |
| arrival_terminal| Arrival flight's terminal |
| arrival_delay| Arrival delay measured in minutes |
| arrival_sch_time| Scheduled arrival time of the flight |
| arrival_est_time| Estimated arrival time of the flight|
| arrival_act_time| Actual arrival time of the flight upon landing |
| arrival_est_runway| Estimated time of arrival at runway |
| arrival_act_runway| Actual time of arrival at runway |
| airline_name| Airline name |
| airline_iata| Airline IATA code |
| airline_icao| Airline ICAO code |
| flight_number| Flight number |
| flight_iata| IATA format of the flight number |
| flight_icao| ICAO format of the flight number |

------

## 200 OK Response Example

```
{
  "status": {
    "message": "Success"
  },
  "results": {
    "status": {
      "message": "Success"
    },
    "results": {
      "airline": {
        "iataCode": "AF",
        "icaoCode": "AFR",
        "name": "Air France"
      },
      "arrival": {
        "actualRunway": "2022-08-11T11:48:00.000",
        "actualTime": "2022-08-11T11:48:00.000",
        "baggage": "05",
        "delay": null,
        "estimatedRunway": "2022-08-11T11:48:00.000",
        "estimatedTime": "2022-08-11T11:43:00.000",
        "gate": "2",
        "iataCode": "ORY",
        "icaoCode": "LFPO",
        "scheduledTime": "2022-08-11T12:00:00.000",
        "terminal": "2"
      },
      "departure": {
        "actualRunway": "2022-08-11T10:35:00.000",
        "actualTime": "2022-08-11T10:35:00.000",
        "baggage": "4",
        "delay": "6",
        "estimatedRunway": "2022-08-11T10:35:00.000",
        "estimatedTime": "2022-08-11T10:30:00.000",
        "gate": "2C",
        "iataCode": "NCE",
        "icaoCode": "LFMN",
        "scheduledTime": "2022-08-11T10:30:00.000",
        "terminal": "2"
      },
      "flight": {
        "iataNumber": "AF6209",
        "icaoNumber": "AFR6209",
        "number": "6209"
      },
      "status": "landed",
      "type": "arrival"
    }
  }
}
```

-------


## Full Documentation

Please visit our [website]( https://aviyair.com/documentation/).

-------
## Historical Flight Delay Data

In addition to the real-time flight delay data, we also have **historical delay data** that you can access. Either combine this with the real-time data or use it individually, historical data is useful in particular for flight insurance and flight delay/cancellation claims. You can visit our [Historical Flight Schedules API repo]( https://github.com/aviyairapi/Historical-Flight-Schedules-API) to find out more about Aviyair's historical delay data.

------

## Most Popular Use Cases

These are the most common use cases for the Flight Delay API but there are no limitations regarding how the API can be useful for you. If you have any concerns about the Terms and Conditions for the real-time flight delay data, you may visit the hyperlink below or contact us to ask about it.

-	Any establishment in charge of airport operation services, either airport authorities or airlines, can use the flight delay data to monitor current flight status and flight delays. This helps manage air traffic at the airport and analyze this data for improving air traffic management in the future. Likewise, this helps improve the overall quality of the airport and maintains a convenient experience for passengers.
-	Flight insurance companies and flight delay compensation services can track delays on their end in real-time, save this data or benefit from Aviyair’s historical flight delay and cancellation data. This way, they can easily maintain demands based on their clients’ requests in a time and cost-efficient way.
-	Airport greetings and other hospitality service providers can track the delay status of their clients’ flights and adjust their operations based on this data. This helps save on costs and manpower and improves customer satisfaction.
-	Flight delay data can be combined with weather data to analyze and provide real-time updates on how weather conditions impact flights. This helps airports and airlines to maintain their operations to avoid any unnecessary delays.
-	Data is always the one essential part of analyzing. Airlines can use the Flight Delay API to track their own performance and see patterns and trends related to flight delays and cancellations. Based on the reports, it is easier for airlines and airports to come up with solutions.
-	Machine learning and analysis projects, powered by flight delay data to predict future average delays and cancellations
- 	Flight schedule tracking for booking or travel websites and apps
- 	Route efficiency analysis from the perspective of flight delays and cancellations

---------

## License

[Terms and Conditions of Use](https://aviyair.com/terms-and-conditions/) apply. If you have any questions or concerns about your use case of the Flight Delay API, please [contact us](https://aviyair.com/contact-aviyair/). 

--------

## How to Access

The API key to access real-time flight delay data is possible by creating an API subscription. The subscriptions do not require any commitments. It is possible to cancel anytime or make changes to your subscription level.

[View the prices and get an API key here.](https://aviyair.com/pricing-subscription-plans/)
