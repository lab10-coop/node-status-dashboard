# ARTIS Network Status Dashboard

Implements a slick web dashboard visualizing the chain status as reported to the included websocket API by network nodes via [node-status-reporter](https://github.com/lab10-coop/node-status-reporter).  

Running instances:
* [ARTIS tau1](http://status.tau1.artis.network/)
* [ARTIS sigma1](https://status.sigma1.artis.network/)

## Limitations

Information shown by this dashboard is not guaranteed to be neither complete nor 100% accurate.  
Only nodes explicitly sending their status to the API are listed.  
Information sent by such nodes isn't verified in any way.  
Locations shown on the map are determined via reverse geolocation by IP (using the [geolite](https://dev.maxmind.com/geoip/geoip2/geolite2/) database), which is not an accurate method.

## Origins

This application was originally developed for Ethereum, with the original repository being: https://github.com/cubedro/eth-netstats.  
It was forked by poa.network and adapted for PoA chains in this repository: https://github.com/poanetwork/eth-netstats.  
From there it was forked and further modified for ARTIS.

## Install

You need node v8 and npm installed and this repository checked out. Then:

```
npm install
npm install -g grunt-cli
grunt artis --configPath="src/js/artisSigma1Config.js"
npm start
```

Now it's running on port 3000, thus you can open it in a web browser at http://localhost:3000

Set the env variable `WS_SECRET` in order to restrict access to the API for reporters.
