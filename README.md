# monzo-hass-sensor
A monzo sensor for home assistant. Currently this can be used to show your current balance as a sensor.

To install this componenet into HASS copy the monzo.py file into a folder called /custom_components/sensor/ in your config directory, then add the following config:

```
sensor:
  - platform: monzo
    client_id: '***CLIENT ID***'
    client_secret: '***SECRET***'
    name: 'Optional name for the sensor'
    cache_path: '/.homeassistant/.optional-cache-location-for-token'
```
   
To get a client ID, and secret go to https://developers.monzo.com/apps/home and click "+ New OAuth Client". Ensure you have set the confidentiality to "Confidential", and set the redirect url to http://ip-of-hass:8123/api/monzo

If you want to use the sensor with multiple accounts ensure you have added all the users to the "collaborators" in the OAuth client registration with monzo, and configure a differant location for the cache_path in hass.

Let me know how you get on!
