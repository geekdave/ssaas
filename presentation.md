background-image: url(horse1.gif)

class: center, middle

???

How to draw a horse

---

background-image: url(horse2.gif)

class: center, middle

---

background-image: url(horse3.gif)

class: center, middle

---

background-image: url(horse4.gif)

class: center, middle

---

class: middle

## 4.

## [ . . . ]

## 5.

???

Something missing between 4 and 5

A lot of technology is like this - leave out the details
I call this the TROLL readme
especially the shitty nitty-gritty details, stuff you're gonna get stuck on

---

background-image: url(ponies.gif)

class: center, middle

???

Right out of the gate -
I work for WalmartLabs and
we kept running into the troll readme with regards to our e2e testing strategy
and it really sucked...

---

class: center, middle

# Dave Cadwallader

.pull-left[![yeah](cowboy2.jpg)]
.pull-right[![yeah](walmartlabs.png)]

???

We create common infrastructure, build and automation tools to support devs working on www.walmart

We follow the test pyramid

---

background-image: url(pyramid.png)

class: center, middle

???

Gaps in UTs - false assumptions between parts of your stack

---

background-image: url(browsers2.jpg)

class: center, middle

???

At walmart - so many browsers
Back to IE8

Pain in the ass to test them all.  Huge waste of time.
Because a pain to test - huge bisect effort
Automation efforts in the past, but all abandoned because they weren't useful.
Why?

---

background-image: url(selenium.png)

class: full-width, left, bottom, white

???

Library with "drivers" for each major browser vendor/version
Deep hooks into browser to "remote control" it over an HTTP API
But... API not friendly

---

background-image: url(sauce.png)

class: left, bottom, white

???

SauceLabs -

---

background-image: url(rube.gif)

class: full-width, left, bottom, white

???

End to end testing like this
tests DSL, translated by test library,

---

class: middle

# **test flake (n)**

# *when your tests sometimes fail for no good reason, creating false positive results*

---

# (see also: *waste everyone's time with this one weird trick. developers hate this!*)

---

background-image: url(ttl.png)

class: full-width, left, bottom, white

???

Fellow teams trying to summit the same mountain

---

background-image: url(sayno.gif)

class: full-width, left, bottom, white

???

1. Slow
2. Unreliable
3. Don't isolate failures

---

background-image: url(challenge.png)

class: full-width, left, bottom, white

???

We got this


---

# Automation Goals

## 1. Dev & QA

???

Non-technical people write tests
Devs run the tests too

--

## 2. Fast

???

Run as part of CI / PR-verify

--

## 3. No flake!

???

Win the hearts and minds

---

background-image: url(nightwatch.jpg)

class: center, middle

???

NodeJS - based adapter for Selenium

---

background-image: url(lion2.jpg)

class: center, middle

???

Got SauceLabs subscription - outsource browsers
Huge collaborative test writing QE/Dev
Turned it on - and...

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

---

![check](check.png)![check](redx.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](redx.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](redx.png)![check](redx.png)
![check](redx.png)![check](redx.png)![check](redx.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

---

10%.....20%.....30%.....40%.....50%.....60%.....70%.....80%.....90%.....100%

![happy](happy.jpg)
???
Got so close - and flake at the end!
--
![happy](happy.jpg)
--
![happy](happy.jpg)
--
![happy](happy.jpg)
--
![happy](happy.jpg)
--
![rage](rage.jpeg)

---

background-image: url(realization.jpg)

class: full-width, left, top

???

We had been thinking of end to end tests like unit tests
Predictable environment that we could control... but nothing like that

---

background-image: url(soup.jpg)

class: full-width, left, top

???

Soup === a test result (binary: pass/fail)

---

background-image: url(cupboard.jpg)

class: full-width, left, top

# Unit Tests

???

Get a result in the safety of your own home
You control the environment - quick & easy

---

background-image: url(car.jpg)

class: full-width, left, top, white

# End-To-End Tests (step 1)


---

background-image: url(zombies2.jpg)

class: full-width, left, top

# End-To-End Tests (step 2)


---

background-image: url(market1.jpg)

class: full-width, left, bottom, white

# End-To-End Tests (step 3)


---

background-image: url(market2.jpg)

class: full-width, left, bottom, white

# End-To-End Tests (step 4)


---

# Lurking Zombies

## 1. Buggy webdrivers

--

## 2. Flakey Network

--

## 3. Service bugs/outages

--

## ???

???

"Test flake" holding back real progress
Seemed overwhelming to fix everything - whack-a-mole.
New problems every day - can't possibly fix all

---

background-image: url(whatif.jpg)

class: full-width, center, middle

???

But what if we could magically make the tests "not flakey" anymore?
...without fixing individual problems?

---

class: middle

# **axiom (n)**

# *...a premise or starting point of reasoning... a premise so evident as to be accepted as true without controversy.*

???

Tool was breaking axiom!
End devs should be able to count on test results as axium
You worry about writing good tests - we worry about infrastructure
The mechanism for achieving, not important
Could be swapped out later.

---

background-image: url(gasp.jpg)

class: full-width, center, middle

???

We did a lot of scary stuff to smooth over these bumps
Retry assertions if they fail, inject
Retry tests themselves if they fail

Important part: MOMENTUM
Smoothing over better than giving up
Not all problems require precision solutions

---

background-image: url(convoy.jpg)

class: full-width, center, middle

???

Is it overkill?  Probably
Is it expensive?  No doubt.
Will fix our reliability problem?  Hell yes!
Anybody watch walk dead? Do they stop for zombies?

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

???

Test reports clean and stable

---

![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)
![check](check.png)![check](redx.png)![check](check.png)![check](check.png)
![check](check.png)![check](check.png)![check](check.png)![check](check.png)

???

If we got a test failure - it's real!

---

10%.....20%.....30%.....40%.....50%.....60%.....70%.....80%.....90%.....100%

![happy](happy.jpg)
--
![happy](happy.jpg)
--
![happy](happy.jpg)
--
![happy](happy.jpg)
--
![happy](happy.jpg)
--
![rage](rage.jpeg)

---

10%.....20%.....30%.....40%.....50%.....60%.....70%.....80%.....90%.....100%

![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](fy.jpeg)

???

When we got to this point... proud of accomplishment, but felt kludgy
duct tape, rubber bands.
"not suitable to release"

---

class: middle

.pull-left[![yeah](fy220.png)]
???
Did we do it with a bunch of clever engineering?  No...
--
.pull-right[![poopsmith](poopsmith.png)]
???
We shoveled shit

---

10%.....20%.....30%.....40%.....50%.....60%.....70%.....80%.....90%.....100%

![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](fy.jpeg)

-----------------------------------------------------------------------------
???
But we thought about our journey, and what would have happened if we hadn't used the axiom hack
--

![happy](happy.jpg)![happy](happy.jpg)![happy](rage.jpeg)

???
And how many others must have tried and given up...
--

![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](rage.jpeg)

--

![happy](happy.jpg)![happy](happy.jpg)![happy](happy.jpg)![happy](rage.jpeg)
???
And how much collective wasted effort has gone into this problem...
---

background-image: url(post1.gif)

class: full-width, center, middle

???

---

background-image: url(post2.gif)

class: full-width, center, middle

???

---

background-image: url(swarm.png)

class: full-width, center, middle

???
Move on to cooler problems! Forked testswarm
Clean reports
First started running on intervals - cuz slow and few resources

---

background-image: url(pr.gif)

class: full-width, center, middle

???

Massively parallel test runner
Remember google criticism? too slow? too hard to isolate failures?
Runs on every PR

---

background-image: url(flakechart1.gif)

class: full-width, center, middle

???
Nagging feeling - what about the flake, sweeping under the rug?
Haven't solved yet - but we can understand it
---

background-image: url(flakechart2.gif)

class: full-width, center, middle

???

By Google giving up, they never get to research the flake
But that's where we're at

---

background-image: url(ship.jpg)

class: full-width, top, middle

# Magellan

???

Code name (for now) - going to open source

End to end test runner - hooks into other libraries such as Nightwatch as plugins.

Not a replacement for nightwatch, protractor, "a test runner-runner"

Commander for your fleet - conductor for your orchestra

Smooth over test flake (but gives insight into what's flakey)
Massively parallel runner
Reporting

---

background-image: url(poopsmith.png)

class: top, center

# \#SSaSS

# **S**hoveling **S**hit as a **S**ervice

???

shovel shit to get here

---

# Shit Shoveling 101

-----------

## 1. Momentum > Perfection

???

Getting stuck on shitty problems is often demoralizing and unproductive

--

## 2. Smoothing Over > Giving Up

???

All those 80% solved problems that never see the light of day

--

## 3. Useful > Precise

???

If you can help someone else smooth over a bump, doesn't matter how much duct tape and rubber bands you have

--

## 4. Open Source > Closed Source

???

Release when it's ready?  Nah- Release when it's useful (even in some small way)
(being a large company, we have a process to follow)

---

background-image: url(battle.png)

class: full-width, left, top, white

# thank you!

# @geek_dave

# ttlpodcast.com

# \#SSaaS


???

Follow me for magellan updates
Come talk to us - Collaborate help build it

---

# Credits

* How to draw a horse

  By: Van Oktop
  http://www.vanseodesign.com/blog/wp-content/uploads/2012/08/browser-logos.jpg

* Zombie Image

  By: Pascal
  https://www.flickr.com/photos/pasukaru76/5067879762

* Soup Image

  By: Keoni Cabral
  https://www.flickr.com/photos/keoni101/5200921858

* Cupboard

  By: Getty Images
  http://abcnews.go.com/Health/Wellness/home-remedies-find-kitchen/story?id=24652838

---

# Credits

* Convoy

  By: DVIDSHUB
  https://www.flickr.com/photos/dvids/5468695790

* Browser Battle

  By: Foice
  http://foice.deviantart.com/art/114-firefox-vs-chrome-212832390
