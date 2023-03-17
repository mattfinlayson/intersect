---
title: monitoring
---

# Notes on monitoring

Metrics That Matter

Actual User Experience

Tail Latency
 - Availability = 1 - (errors + slow responses)
 - If 1 in 30 times the response is slow and times out users will call that an error. Deal with it.
 - Users will probably reload at about 3x - 5x median latency.

Service efficiency
 - Normal: 
	 - Take historical demand
	 - extrapolate forward
	 - Add inorganic changes (now it takes 2 api calls or whatever change you’re making)
	 - Divide projected demand by efficiency and secure resources
 - Sad Panda - you change the service all the time
	 - Benchmark before major releases, on an interval, or during big changes
	 - Even minor changes can make big perf changes
	 - Common ways to find efficiency has changed is an outage (we thought we have n+2, but we had n + 0.5 and ate shit)
 - Solution
	 - Daily benchmarking on service efficiency
	 - If you purchase fixed assets you need this to prevent outages
	 - Even if you have a cloud provider you need it to keep costs under control.


# Notes on SRE

key pieces include status parity, free transfer, scarcity, operational load caps, error budgets

availability
latency
performance
efficiency
change management
monitoring
emergency response
capacity planning

SRE has quarterly service reviews
 - designed to measure ops workload
 - 50% time doing development

The business or the product must establish what the availability target is for the system. Once you've done that, one minus the availability target is what we call the error budget; if it's 99.99% available, that means that it's 0.01% unavailable. Now we are allowed to have .01% unavailability and this is a budget.
SRE no longer has to apply any judgment about what the development team is doing. SRE measures and enforces, but we do not assess or judge. Our take is "As long as your availability as we measure it is above your Service Level Objective (SLO), you're clearly doing a good job. You're making accurate decisions about how risky something is, how many experiments you should run, and so on. So knock yourselves out and launch whatever you want. We're not going to interfere." And this continues until you blow the budget.

It is crucial that you establish what the target SLO is upfront, because that is the standard against which you are agreeing that the service will be measured. SRE is at that point simply measuring and enforcing something we've already agreed we want. Very handy position to be in.

Monitoring

So there are, in my view, only three kinds of valid monitoring output. There are alerts, which say a human must take action right now. Something that is happening or about to happen, that a human needs to take action immediately to improve the situation.
The second category is tickets. A human needs to take action, but not immediately. You have maybe hours, typically, days, but some human action is required.
The third category is logging. No one ever needs to look at this information, but it is available for diagnostic or forensic purposes. The expectation is that no one reads it.

There is mean time between failure
mean time to repair

https://docs.google.com/document/d/199PqyG3UsyXlwieHaqbGiWVa8eMWi8zzAn0YfcApr8Q/preview
http://www.standalone-sysadmin.com/blog/2014/06/the-difference-between-site-reliability-engineering-system-administration-and-devops/