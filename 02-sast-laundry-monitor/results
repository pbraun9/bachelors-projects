# sast-laundry-monitor

## tools

nice to have four tools compared at once.
would checkov[^checkov] possibly also fit in this list or does it belong to another cathegory?

[^checkov]: https://github.com/bridgecrewio/checkov

## ci/cd

seems those are all static scans made against images not dynamic against containers, so the title in scan.yml doesn't match.

	name: Container Security Scan

I hope it clear to you what is the difference between images and containers

it might be worth considering doing the security scanning outside of pipelines in case it slows them down.
there is usually a balance to find between security and usability.
here it's between security and productivity for developpers.
fast pipelines are cool.
in a nutshell, it would have been great to have an additional point to consider offline scanning and how to replace ci/cd with cron jobs and such for that purpose.

## vuln finding results

as discussed during presentation, it's a bit strange you show only results after vulns have been fixed, resulting in many empty results (zero for almost all but Grype).
it would have been preferable to show the table of results also _before_ intervention, so we can compare.
this was mentioned during presentation q&a

also it would have been preferable to describe those remaining vulns after the fixes.  is Grype better than the other or actually providing noise, false-positives, or neutral-positives (the latter would be a good thing)?

## fixing vulns intervention (key fixes)

nice job!  nice two tricks!

what about "forcing updates", how and where was this done?

## remaining issues

you need to describe the vulns that remain and eveluate the risk.
what severity?
are you impacted by the vuln?
(sometimes, and even often, we are not affected for some reason, so it can be considered benign/neutral positive.

## ccl

I got that combining tools improves accuracy,
however it's still not clear which tools are good or bad **as a conclusion**,
regarding their results.
you only mentioned the differences of the tools in the "tools description" section.

