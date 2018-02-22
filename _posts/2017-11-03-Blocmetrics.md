---
layout: post
title:  "Blocmetrics"
image: blocmetricsHome.png
---

## Summary
Blocmetrics is an analytic service that offers a few valuable key features.


## Explanation
* A client-side JavaScript snippet allows a user to track events on their website, by adding the following snippet to the user website into their  "app/assets/javascripts/application.js" file:

{% highlight ruby linenos=table %}
 var blocmetrics = {};
   blocmetrics.report = function(eventName){

    var event = {event: { name: eventName }};

    var request = new XMLHttpRequest();

    request.open("POST", "https://ehayes-blocmetrics.herokuapp.com/api/events", true);

    request.setRequestHeader('Content-Type', 'application/json');

    request.send(JSON.stringify(event));
   };
{% endhighlight %}

## then enter this event report in any view

{% highlight ruby linenos %}
 <script type='text/javascript'>
   blocmetrics.report('event name');
 </script>
{% endhighlight %}

![Event](/images/blocmetricsEventsDone.png)


* A server-side API that captures and saves those events to a database.

* A Rails application that displays the captured event data for a user.

* A user can sign in and out of Blocmetrics providing an email and password.

* A user can register an application with Blocmetrics for tracking.

* A user can view a graph of events for each registered application.


## We tested the API by using curl:

{% highlight ruby linenos %}

 $ curl -v -H "Accept: application/json" -H "Origin: http://registered_application.com" -H "Content-Type: application/json" -X POST -d '{"name":"click"}'  https://ehayes-blocmetrics.herokuapp.com/api/events>
{% endhighlight %}
