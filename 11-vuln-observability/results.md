# vuln-observability

good job with defectdojo

ok I see a dashboard visualization for "suspicious requests by container"

NOK why are the diagrams referring to Filebeat while you used Fluent-bit?
(in README `Methods`)
-- same in README `5) Observability Pipeline`

Following questions are rethorical...

> Would you actually use this architecture and observability methods in production?

I suppose not, because it doesn't seem to be anwhere close to something that could actually be truly useful.  It's not just about the missing traces nor the limits of the dashboard and automated scan-to-report you've designed.  It's an overall problem that it's hard to merge all those different types of data, because they leverage different tools.  That's the conclusion you might have been able to reach, instead of trying to make it happen.  You've been confronted to an architectural problem and didn't talk about the issue.

> Do you believe you've actually solved the issue of possible conjuction of various types of data to be centralized in a single place?

I suppose not because you can't mix metrics, logs and traces in the same place.  Well actually since ELK v8 there's a way to do metrics, but I didn't see this mentioned either.  It doesn't scale as well as dedicated metrics storage anyway like Victoria Metrics and such.

