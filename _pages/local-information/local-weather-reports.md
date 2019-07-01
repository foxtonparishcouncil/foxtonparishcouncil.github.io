---
title: "Local Weather Reports"
permalink: /local-information/local-weather-reports
historic_url: http://foxtonparishcouncil.gov.uk/feeds-weather.php?id=9
layout: simple
sidebar:
  nav: local-info
---
<style>
.archive {
padding: 0 !important;
}

</style>


## BBC Report

**This page is a work in progress!** <br> The weather feed on our website has been broken for quite sometime - hopefully it will be working again soon.
{: .notice--warning }

<div class="bbc-weather">Loading the JSON feed from the BBC… </div>


<script defer async="false">

var bbcWeather = function($) {
        // m.highways.gov.uk
        
        var url =  'https://weather-broker-cdn.api.bbci.co.uk/en/forecast/aggregated/2649116';
        var display = $('.bbc-weather');
        $.ajax({
            url: url,
            type: 'GET',
            dataType: "json"
          })
          .done(function(feed) {
          
          display.html('<p>Loaded the JSON feed from the BBC…</p>');
          display.append(feed.forecasts[0].summary.report.enhancedWeatherDescription);
          display.append('<br>');
          display.append(feed.forecasts[0].summary.report.windDescription);
          
          console.log(feed.forecasts[0].detailed.reports[0])
          
          })
          .fail(function(){
            display.hide();
          });
          
};

Namespace.Deferred.execute(bbcWeather);


</script>

<!-- https://www.metoffice.gov.uk/weather/forecast/u1202y5ms#?nearestTo=Foxton&date=2019-06-18 -->