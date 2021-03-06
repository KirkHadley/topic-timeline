# Topic Timeline

This timeline shows representative New York Times stories for a chosen keyword using data from the New York Times' Article Search API.

Topic Timeline is an AngularJS directive that can be embedded as a widget or used
as part of a larger Angular app. It was created for the New York Times' [TimesOpen Hack Day 2013][hackday2013].

## Dependencies
You'll need 
[AngularJS][AngularJS] and [TimelineJS][TimelineJS].

Topic Timeline uses the New York Times [Article Search API v2][article-search-api]. 
[Request an API key][request-api-key] from the NYT. Be sure to get a key for the 
"Article Search API."

## Demo

See a demo at 
[http://chc.name/dev/topic-timeline](http://chc.name/dev/topic-timeline)

## Installation

Include AngularJS, TimelineJS, and `topic-timeline.js` in your HTML file,
in that order: 

```HTML
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.7/angular.min.js"></script>
<script src="http://cdn.knightlab.com/libs/timeline/latest/js/storyjs-embed.js"></script>
<script src="topic-timeline.js"></script>
```

In the opening tag of your `<body>`, add the attribute `ng-app="topicTimeline"`:

```HTML
<body ng-app="topicTimeline">
    ...
```

Now add a `<topic-timeline>` element to your HTML wherever you'd like to embed the
timeline, setting the `search-term` and `api-key` attributes:

```HTML
<topic-timeline search-term="food" api-key="YOUR_NYT_API_KEY_HERE" />
```

See [`example.html`](./example.html) for an example.

### Variations

If you prefer, you can also use the directive as an attribute:

```HTML
<div topic-timeline search-term="food" api-key="YOUR_NYT_API_KEY_HERE" />
```

If you're already running and Angular app on the page, include the `topicTimeline`
module as a dependency of your main app when you declare it in JavaScript. In this 
case, do not use the `ng-app="topicTimeline"` 
attribute on the `<body>` tag:

```JavaScript
var myApp = angular.module('myApp', ['topicTimeline']);
```

[AngularJS]: http://angularjs.org/
[TimelineJS]: https://github.com/NUKnightLab/TimelineJS
[hackday2013]: http://open.blogs.nytimes.com/2013/11/22/timesopen-hack-day-2013/
[article-search-api]: http://developer.nytimes.com/docs/read/article_search_api_v2
[request-api-key]: http://developer.nytimes.com/docs/reference/keys

