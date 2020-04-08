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