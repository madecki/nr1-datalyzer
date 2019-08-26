# Datalyzer

Explore, slice and dice dimensional metrics with this handy NerdPack

Author: Lew Cirne

## Screenshot
![screenshot](./screenshots/screenshot.png)

## Running Locally

Current status of the UI is very rough and unintuitive. Given that caveat:

Run the following scripts:

```
npm install
npm start
```

<<<<<<< HEAD
Open https://staging-one.newrelic.com/?packages=local

You can select an account and metric in the two dropdowns at the top of the window. I haven't
yet figured out how to make those dropdowns show the default selection to start.

Pick a metric name (I always start with "container" to look for interesting stuff).

On the left, you'll see a set of _dimensions_ and _attributes_:
- Dimensions are facets that apply to this specific metric, with a cardinality of greater than 1.  The cardinality of each dimension is displayed to give the user a hint about what dimensions might be "interesting".
=======
Open https://one.newrelic.com/?packages=local

Pick an account, and select a metric or event data to plot.

On the left, you'll see a set of _dimensions_ and _attributes_:
- Dimensions are facets that apply to the selected metric/attribute, with a cardinality of greater than 1.  The cardinality of each dimension is displayed to give the user a hint about what dimensions might be "interesting".
>>>>>>> metrics-and-events
- Attributes are facets with a cardinality of 1. (There's no use in faceting by an attribute
with a cardinality of 1, you will just get teh identical data. So just show the single for that attribute.)

## Where it could go
There's lots of overlap between this and the chart builder, so I can imagine this gets shelved when 
we add support for dimensional metrics in the chart builder.

That having been said, really like the usability beneifts that come with seeing all of
the relevant  facets/dimensions, with cardinality, on the left. And calling out 
a facet with a cardinality of 1 as just an attribute of the data set.  So maybe
we look to incorporate some of these ideas into the core product.

We could apply many of the same UI concepts to an event data analyzer too.

However, this thing is unlikely to become a very useful package until/unless the user can 
take some sort of action on the generated charts. The default actions (add to dashboard, etc)
would go a long way!!

## TODO
- Obey time picker
- Embed in explorer for APM/APPLICATION, MOBILE/APPLICATION, INFRA/HOST, etc

