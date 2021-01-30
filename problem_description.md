
i have frequencies to talk to and from a satellite. 
My goal is to know where to point an antenna, and what frequencies to tune to talk with that satellite.

the satellite has the usual TLE data https://en.wikipedia.org/wiki/Two-line_element_set

I have a dict with current GPS time and location, including altitude

i want to know azimuth, elevation, distance, and closing speed of the satellite to me.
(Azimuth is in true north.)

relative speed to me, so i can calculate the doppler offset

bonus points for doppler from that closing velocity, and higher points for calculating the frequency curve over time.

example data:
```
ISS (ZARYA)
1 25544U 98067A   21023.70745294  .00000455  00000-0  16460-4 0  9991
2 25544  51.6465 337.3326 0002215 283.5447 140.1129 15.48878572266208
```
my position: 41.6728150, -70.4630193, 100 ft msl
and calc for a time like 2100 UTC today.

https://spaceflight.nasa.gov/realdata/sightings/SSapplications/Post/JavaSSOP/SSOP_Help/tle_def.html
https://live.ariss.org/dashboard/esamap/

live tle: https://live.ariss.org/iss.txt

https://en.wikipedia.org/wiki/Simplified_perturbations_models (edited) 

https://space.stackexchange.com/questions/31174/differences-between-sgp8-and-the-standard-sgp4-is-it-ever-used-in-practice (edited) 


Possible examples:
```
from_gps = {lat:0, lon:0, alt:0, time:1611967307.1238900}

function( from_gps, sat_tle ){
```
