# idor-n-jwt-pvs-studio

---
slides & report

nice vuln/weaknesses to test against

ok slight descr of the two vulns to begin with

it is sad that pvs-studio doesn't include those rules by default, isn't it?
why do we have to write custom rules for such dramatic flows?

==> ok section 3.6 - you are pointing out the problem that pvs-studio is not efficient by default

(just a question: aren't other SAST tools able to detect those flaws either by default?)

==> ok section 4.3 that got answered

ok good acceptance test: without custom rules than with custom rules

nice walkthrough on IDOR, thank you

nice walkthrough on JWT alg flaw

---
code & demo

?? not sure why there is a hard-coded secret value in the code `JwtAuthConfig`
-- mhm maybe that's exactly what we need to test against to validate alg=none

---
conclusion

I don't have much to criticize apart from the presentation's sketchiness and lack of clarity.
looking at the report and some glance at the code looks like serious.
good job!!

if you are not happy having a 10, I suppose we will be able to dig more and find some weaknesses tho)  as a joke and response to your last slide (I didn't see any number there).

