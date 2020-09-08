# Use Event Handlers with React

> Application’s can be laid out and styled pretty, but if they don’t respond to interactions from the user then they’re just web pages, not apps. Let’s get an introduction to event handlers with React. There are a ton of supported events that you can find on the docs. We still haven’t gotten to state yet, so we’ve implemented our own little way of managing state and re-rendering our component so we can play around with event handlers.

One thing you’ll want to know is that events with React are very similar to working with events in regular DOM. React does have an optimization implementation on top of the event system called SyntheticEvents, but most of the time you won’t observe any difference with those events from regular DOM events (and you can always get access to the native event using the nativeEvent property).
