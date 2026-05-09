# fuzzing heartbleed

---
slides

NOK a better description of the heartbleed vuln would have been good.
the problem is not just for servers but also for clients.
also it's not just TCP but also UDP (DTLS).
you should to be clear on what are you targetting before fuzzing it.

ok the main thing is that it's about reaching client or server's memory, indeed.

ok you described what function calls you are fuzzing,
`ssl_d_handshake` and `SSL_read`

ok you discuss how the vuln got fixed

---
report

ok there are well enough technical details there!

ok good job ok building openssl statically

ok good job with linking those static libs into the fuzzer

I am not sure exactly yet what we're finding with your results,
it would require me to spend way more time on it,
but I see genuine work has been done, congrats.

the only weak point was during presentation, it was not clear what you're demonstrating while showing the demo, but otherwise we are good.

