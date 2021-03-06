# changelog

What's changed on [uptimeumbrella.com](https://uptimeumbrella.com)?

#### 10/25/2016 - Shorten notifications and more calibration for network flapping

We noticed that some of our text messages were being sent as multipart.
Turns out, SMS messages that contain special characters, like emojis, are only allowed a length of 67.

We also tweaked the ping algorithm to be even more lenient for network flapping.
When we encounter a failed ping we now immediately retry to make sure it wasn't a fluke.

#### 10/18/2016 - Increase timeout and retries

In order to account for hiccups on the internet, we've bumped up the retry count to 2 retries and the timeout to 10 seconds.
Previously we had the retry count set to 1 and the timeout set to 2 seconds which was a bit too ambitious.
Now our users shouldn't get notifications when our ping microservice has to take the long road from server to server.

#### 10/11/2016 - Fix a phone number validation bug

We fixed a bug that caused phone number validations to not work correctly.
This ensures that registered users have valid numbers so we can send them notifications.

#### 10/10/2016 - Add an FAQ page

We've added an FAQ link at the top of the page to aggregate some of the questions we've been receiving. We'll add to this page as new questions come in.

#### 10/6/2016 - Bring downed urls to the front

We hope it's rare when your site goes down.
But, when it does, we bring it to the top of the UI so you can be reminded to run that migration, `./kick.sh`, redeploy or whatever it is you need to do.

![qlv9noezbin72qnixqmdghnxeiblutxr5djpksbhvta](https://cloud.githubusercontent.com/assets/1424573/19172033/0cbac19e-8bdd-11e6-8ff2-9a4de6446b70.png)

#### 10/4/2016 - Improve aesthetics and the wizard flow

The MVP had a pretty clunky onboarding flow so we cleaned it up a bit.
Thanks to everyone that gave us great feedback.

The header display for the latest ping is now nicely formatted with a touch of syntax highlighting.
No more raw json blobs.

#### 10/3/2016 - A couple bugs

We fixed a pretty serious bug that caused our billing integration to sporadically fail.
Turbolinks + Stripe = 💔.

Pinging is now 5 times faster, before we retried every `HEAD` request a ridiculous five times before failing.
You now get a text message after one retry (we still don't want to send you a text for a minor hiccup).

We also changed some messaging and forced `https`.

#### 10/2/2016 - The beginning

First launch 🚀.
