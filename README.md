# A Home assistant custom component to get your fitness information using Google Fitness API.


To get started put all the files from`/custom_components/google_fit_hass/` here:
`<config directory>/custom_components/google_fit_hass/`

**Example configuration.yaml:**

```yaml
sensor:  
  - platform: google_fit
    name: hemant
    client_id: !secret google_client_id
    client_secret: !secret google_client_secret
    scan_interval: 300
```

At the moment, provides following measurements:
```yaml
    - steps
    - distance
    - time
    - calories
    - weight
    - height
    - sleep
    - heartrate
```    

Sensor is designed to be flexible and allow customization to add new Google Fit
dimensions with minimal effort with relative knowledge of Python and Fitness
Rest API.


In order to generate your client_id and client_secret, see the prerequisites
for Google Calender component:
https://www.home-assistant.io/components/calendar.google/#prerequisites

To make sensor work you have to enable Fintness API in your project.
In oder to enable Fitness API open Google cloud console: 
https://console.cloud.google.com/apis/library/fitness.googleapis.com
and enable API.

It is recommendable to store client_id and client_secret as secret as
possible. You can read about it on:
https://www.home-assistant.io/docs/configuration/secrets/