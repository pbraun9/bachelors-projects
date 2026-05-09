# social login

---
report

ok the keyword -- "identity provider" -- is there

ok explanation about difference with TG vs OAuth2: a bot is required
-- the drawback for this is that it is not possible to do SSO at the same time
-- can't be Keycloak be put in between anyways?

ok the authentication flow diagram is cool

?? about 2.3 TG verification
-- not sure how the backend verifies the bot token nor the user
-- it is calculating hmac-sha2 based on what?

ok even session mgmt is explained

NOK the report looks like an utterance/list of things to consider from AI without the need to actually consder it!  What do all those point mean?  What do they imply?  It's fine for some sections which can be considered nice bonuses for the reviewer, but not for section 4.2 security measures!
also authentication process aspects should be apart from other aspects

NOK section 4.3 says sessions not persistent, that contradicts

---
slides

ok here is explained how HMAC is used (page 6): the bot token is used for payload integrity
-- and it is also explained that the bot token is known only to the backend (page 3)

still I would need resources and links to TG's specs on that

---
demo

thanks for delivering a video

NOK the authentication process is not very verbose,
what happens if the user is NOT connected to TG just yet?  this was not shown (also discussed in q&n during presentation)

NOK also for acceptance testing user-data access, it would have been preferable to re-login with ANOTHER USER and show its notes.

---

UPDATE: thanks for the specs

fw https://core.telegram.org/widgets/login-legacy
fw https://core.telegram.org/bots/tutorial

- nothing about BotFather peering with your domain
- what domain did you use?

==> ok clarified in private msg, that's actually conceivable that it worked with localhost
-- while checking the authentication flow, the FE is indeed just a client to the TG bot

- where is the code for the Minimal Working Example (MWE) bot that you've used?

==> the team decided to focus on the FE and BE logic, however the whole picture is mainly between your app and TG and that was also important.

