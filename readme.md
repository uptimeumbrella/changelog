# changelog

What's changed on [uptimeumbrella.com](https://uptimeumbrella.com)?

#### 10/2/2016 - A couple bugs

We fixed a pretty serious bug that caused our billing integration to sporadically fail.
Turbolinks + Stripe = 💔.

Pinging is now 5 times faster, before we retried every `HEAD` request a ridiculous five times before failing.
You now get a text message after one retry (we still don't want to send you a text for a minor hiccup).

We also changed some messaging and forced `https`.

#### 10/1/2016 - The beginning

First launch 🚀.
