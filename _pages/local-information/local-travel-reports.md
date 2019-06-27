---
title: "Local Travel Reports"
permalink: /local-information/local-travel-reports
historic_url: http://foxtonparishcouncil.gov.uk/feeds-travel.php?id=10
layout: simple
sidebar:
  title: "Local Information"
  nav: local-info
---
<style>
.archive {
padding: 0 !important;
}

</style>


## Local Highways Agency Road Travel Report

**This page is a work in progress!** <br> The traffic feed on our website has been broken for quite sometime - hopefully it will be working again soon.
{: .notice--warning }

<div>
<h2>South East Region</h2>
<div class="south-east">Loading…<br>South East Region RSS from Highways England</div>
</div>

<div>
<h2>Eastern Region</h2>
<div class="eastern">Loading…<br>Eastern RSS from Highways England</div>
</div>

<script defer async="false">

var runMyCode = function($) {
        // m.highways.gov.uk
        loadFeed($('.south-east'), 'https://m.highwaysengland.co.uk/feeds/rss/AllEvents/South%20East.xml');
        loadFeed($('.eastern'), 'https://m.highwaysengland.co.uk/feeds/rss/AllEvents/Eastern.xml'); 
};

Namespace.Deferred.execute(runMyCode);


</script>