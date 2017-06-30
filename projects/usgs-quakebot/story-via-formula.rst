*****************
Story via formula
*****************

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


http://www.latimes.com/local/earthquakes/

http://www.latimes.com/local/lanow/la-me-earthquakesa-earthquake-42-quake-strikes-near-petrolia-calif-xz2i-story.html


    A shallow magnitude 4.2 earthquake was reported Saturday afternoon two miles from Petrolia, Calif., according to the U.S. Geological Survey. The temblor occurred at 2:22 p.m. PDT at a depth of 5.0 miles.

    According to the USGS, the epicenter was 17 miles from Rio Dell, Calif., 20 miles from Ferndale, Calif., and 35 miles from Eureka, Calif.


http://www.slate.com/blogs/future_tense/2014/03/17/quakebot_los_angeles_times_robot_journalist_writes_article_on_la_earthquake.html


    A shallow magnitude 4.7 earthquake was reported Monday morning five miles from Westwood, California, according to the U.S. Geological Survey. The temblor occurred at 6:25 a.m. Pacific time at a depth of 5.0 miles.


    According to the USGS, the epicenter was six miles from Beverly Hills, California, seven miles from Universal City, California, seven miles from Santa Monica, California and 348 miles from Sacramento, California. In the past ten days, there have been no earthquakes magnitude 3.0 and greater centered nearby.


    This information comes from the USGS Earthquake Notification Service and this post was created by an algorithm written by the author.

    Read more about Southern California earthquakes.


https://mobile.twitter.com/earthquakesLA/status/445552031311220736


USGS version:

https://earthquake.usgs.gov/earthquakes/eventpage/ci15476961#executive




Logic:


- Calculate depth (under 10km or more) https://apnews.com/d4217c33c5124972845022441d69728c/ap-explains-difference-between-shallow-deep-earthquakes
- Calculate magnitude
- Calculate day of week from 2014-03-17 13:25:36 UTC
    https://davidkeen.com/blog/2017/01/time-zone-conversion-in-google-sheets/
    https://support.google.com/docs/answer/3094139?hl=en
- Calculate Pacific time from 2014-03-17 13:25:36 UTC
- Convert depth from km to miles


The raw data:

time,latitude,longitude,depth,mag,magType,nst,gap,dmin,rms,net,id,updated,place,type,horizontalError,depthError,magError,magNst,status,locationSource,magSource
2014-03-17T13:25:36.870Z,34.134,-118.4861667,9.245,4.4,mw,208,40,0.0379,0.28,ci,ci15476961,2017-04-18T19:22:38.648Z,"3km SSE of Encino, CA",earthquake,0.18,0.31,,6,reviewed,ci,ci




=ROUND(D2*0.621371, 1)






