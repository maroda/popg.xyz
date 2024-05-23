---
title: "Exercise: Wheel of Expertise"
description: Dive deep into specific subjects to share mental models.
author: craquemattic
type: post
date: 2024-05-23T00:05:05Z
url: /2024/05/23/wheelofexpertise/
categories:
  - training
  - exercises
  - operations
tags:
  - humanfactors
  - resilience
  - knowledge
toc: false
---
# Spin the Wheel of Expertise!

## Requirements

* People: **3-25**
* Timebox at **30-90m**
* Facilitators: **1**
* Themes that contain expertise: **6-12**
* "Carnival wheel" with empty pie slices (physical or virtual)

## Facilitator Instructions

### Session Setup

This game was developed on a small [physical carnival wheel](https://www.amazon.com/Brybelly-Customizable-Adjustable-Tabletop-Parties/dp/B07TZS1RTG/>) with a whiteboard surface.

Divide the face of the Wheel into equal sections. In each, place a one- or two-word theme that connects with some aspect of the complex-system-at-large. These can be anything from a specific technology ('bucket', 'cache'), a layer of your stack ('Service', 'API'), a process ('failover', 'restoral'), and so on.

Fill the Wheel with these terms, somewhere between six and a dozen should be enough to fit. If the game is being played remotely, whoever has the Wheel is the proxy-spinner for each person on the video call.

### To Start

1. Introduce the game with the sections already filled out.
2. Volunteer to go first.
3. Spin the **Wheel of Expertise** (WoE) to get a new term for exploration.
4. Show _by example_ how you would dig deeper into this term. If you are a novice, show what you'd do to learn more. If you are the expert, guide us through what you know.

   * Share your screen.
   * Talk through what you're doing.
   * Do what you'd really do to figure this out under pressure, i.e.: "In an incident, how would you quickly learn more about this?"
   * Ask for help if you get stuck.
   * Each player has ~10m to play.

### To End

There is not a real finite close to this activity, typically the timebox ends and the current discussion is wrapped up.

Do some sort of write-up about the session and post it in whatever shared chat channel this community of practice uses. Depending on what your Slack @mention culture is, give people credit for participating. Some examples of this appear below.

Tips on guiding this activity:

* Encourage conversation, this is not a test. A good prompt is: "Show us what you know about this from your perspective, and how you'd learn more."
* This is not a technique for putting people on-the-spot. Those not comfortable with doing this activity should not be required to do it, observers are welcome.
* Decide if you want to replay themes (which can be interesting on its own) or always spin for a new one (which will reduce choices as the game progresses).
* Always encourage players to ask for help if they get stuck. We are here to share.
* Respect the time to let enough people, if not everyone, have a chance to spin.
* Give the deep-dive a timebox itself, no longer than 10-15m. This might be challenging, an expert may have a lot to say about their area and might need to be reminded of the time.
* Conversely, the conversation could become helplessly engaging as new things are discovered. This is exactly the time "to get in the weeds" about it, being flexible about the length of each turn is perfectly acceptible.

## Example Activity

### No. 1: Who, What, Where

The first version of this game asked to pick a question to answer about the theme, in the form of: "who?", "what?", or "where?". Every participant chose "what" and it became evident that this granularity of questioning wasn't necessary: picking "what" implied "how" which covered most cases of "who" and "where". From this point forward, the game was simply known as **Wheel of Expertise**.

The themes you see are code names for different parts of the application stack: *Atlas / Locko / Blueprint / Incident / Blamo / Resto / IAM*

{{<figure width=200 src="/2024/05/23/wheelofexpertise/wheel_no1.jpg" title="WoE the First" alt="Wheel of Expertise, Nov 2021" >}}

#### Summary of Gameplay

> The gameplay is like this: Willing participants spin the wheel. Where it lands on one of our mission critical services, they get to choose: Who, What, or Where. Then they give an answer by sharing their screen and showing their process for finding the answer. They then call on the next participating wheel spinner. They get no help unless they "escalate" and ask for it!
>
> For this session, "What" became an overriding theme. Which was great as we dove into these services learning what they did, what they contained, what they talked to, and what outcomes (or bugs!) they produce. Today we covered (and often made connections between): Blamo (`@_user1`), Resto (`@_user2`), Locko (`@_user3`), Blueprint (`@_user4`), and "IAM / RBAC" (`@_user5` with an assist by `@_user6`). The wheel did not allow us time with Atlas or Incidental, but there's always future sessions! `@_user7` provided a lot of great input and perspective with deeper questions, and I helped move the discussion along and timeboxed.
>
> One of my favorite parts of this exercise is not only just hearing the answers, but also the sharing of how people find them. Learning from someone's expertise is often not the answer itself, but peeking inside their mental model and process in coming up with answers... or more questions. This included where people turn first for answers and where they go next when stumped, but also even how we use Zoom to collaborate.
>
> *-- Matt Davis, Autumn 2021*

### No. 2: The Sharp End of Storage

Diversity is an important aspect of Practice of Practice Gamelan. In addition to SREs and developers, we had regulars from Product and Marketing and Customer Support. Expanding on the original concept, themes were crafted to allow both technical and non-technical perspectives depending on the expertise and background of the attendees. We wanted to help non-technical people feel they could contribute to the session.

The resulting themes are more generic: *Runbook / Error / Search / Cert / Image / Login / Deploy / Queue / RBAC / Bot / Comm / Node / Jira / SDM*

{{<figure width=200 src="/2024/05/23/wheelofexpertise/wheel_no2.jpg" title="WoE the Second" alt="Wheel of Expertise, March 2022" >}}

#### Summary of Gameplay

> Preparing for today's Practice of Practice Gamelan I was thinking about two things: sharp-end work and ambiguity. I set out to create a Wheel of Expertise that matched, but wasn't sure if the concept would work out or not. By all accounts, I think it did. Our session was a comfortable chamber quartet, with `@_user1` randomly spinning the wheel to CERT (not staged! we swear!), `@_user2` landing on IMAGE, `@_user3` driving into DEPLOY, and `@_user4` with the noble ERROR.
>
> This is the conversation about IMAGE that took us through a deep dive of our storage buckets in GCP.
> Wow. Talk about some deep-diving, sharp-end marvelousness. We stuck with a semblance of the "what?" about these topics, but really it felt a lot more natural than that. We simply took the word and applied it to our own perspective or experience in our work.
>
> To give you a taste: CERT may seem pretty obvious to the guy who refactored our cert-manager system, certainly we got an even more detailed view of what happened in the demo. But ERROR? We got a tour of a sequence of terraform + GCP errors that `@_user4` just dealt with in Terraform Cloud. DEPLOY? `@_user3` treated us to a CircleCI problem he had the pleasure of wrestling with SRE. IMAGE? `@_user4` admitted, he would have gone the route of our Google Container Registry and docker... but this was after `@_user2` had taken us through a discovery of the many pieces that come together to store a customer image on the incident timeline (a lot of which I didn't know and we all discovered together!!!).
> This was an amazing journey today through a lot of things we discovered along the way. Every single one of us was displaying our own ways of digging the system. We commented several times how nice it was to be able to explore these things in this way outside of cognitive stress and the pressure of an incident.
>
> *-- Matt Davis, Spring 2022*

### The Storage Bucket Incident

As you may have guessed, an incident involving the system of the second example occurred not more than a month after we had the session. The SRE On-Call during the incident was present at PoPG that day. All of that detail digging and context uncovering about a legacy service nobody knows that becomes so stressful and haphazard during an incident... it already got done. We did it, slowly, together, without any production pressure.

An important aspect of building functions like *Practice of Practice Gamelan* is that the organization not only supports the effort, it makes room for the effort to have wings. The things we do in Operations that do not contribute to Feature development are traditionally difficult to get prioritized. Applied Resilience Engineering activities like this and Incident Learning Reviews are considered "expensive activities" because they are not leveraging the "raw talent" of the people involved.

Put another way: if you're playing a game about incidents for an hour, that means you're not able to code for that hour. A quantitative Return on Investment for Resilience Engineering is difficult to see, to someone counting the numbers it can feel a lot like buying insurance. Seen in that light, I would judge that we saved no less than the time it took for the session to happen, maybe double, on our "time to clarity" for whatever the hell was going on with this system. Two or three hours given back is a solid quantitative measure for ROI, especially during incidents where _seconds_ matter.

### No. 3: Spawn of the Wheel

The format of **WoE** became a regular go-to for our _Gamelan_ and created several spinoffs. One of them developed into a full-fledged incident training exercise called **The Great Incident Baking Show**. The goal of the exercise is to use real tooling and real alerting to practice real declaration of incidents that use all the 'production' services that would be touched in a real event: the alerting platform, the incident management platform, the ticketing platform, the chat platform, and the processess themselves.

I recall the attendees joking that we were "Chaos Engineering our incident process", and that's pretty spot-on for what went down. We not only practiced the process, we dug into bugs in our platform. In fact, **Practice of Practice Gamelan** is a wonderful place to merely use the tools we leverage for coordination, communication, and collaboration. There were times that we experimented with what we could accomplish with Zoom and times that we were learning its features together.

That's a more reliable, distributed style of training than deferring any learning for actual incidents. While there are opportunities to learn during accidents, the ability for people to learn drops while we are under stress or trauma. What humans pay attention to in these circumstances is volatile, what they remember even moreso. We can indeterminately learn by being dropped into a stressful situation, but if we can learn these things without production pressure we can more easily avoid becoming traumatized about it (skipping the learning entirely). Plus, we can emphasize the things we _want_ to focus on learning, because such things may not ever come up if we wait for just the right incident.

Themes for this were bigger, our 'argot' (or jargon) for the following: **ServiceNow integration / Incident Tags / Event Driven Updates / Trial Clusters / Microsoft Teams integration / Slack integration / Communication Workflows**

#### Summary of Gameplay

> "In *Practice of Practice Gamelan* this week we got out the _Wheel of Expertise_ and used it to drive a hands-on exercise: _Declare an Incident in Our Platform_. This was a time for attendees to experience declaring incidents. To my surprise, the majority of the Gamelan had not! So we did skew the activity to those who haven't had the opportunity.
>
> A very special shout-out to `@_user1` and `@user_2` from the Go-To-Market team who may not have known what they were getting themselves into! Y'all did awesome. I confess I put `@user_1` on the spot first, but not arbitrarily. As our new Product Marketing lead, I saw an opportunity. So he led by performing some configuration on a new _incident Type_ we are using for this session.
>
> We covered several configuration topics, learning some of the gotchas that hit us when we try to accomplish "Work-as-Done" and butt up against incongruent "Work-as-Imagined" or "Work-as-Prescribed". This was illuminating, raising questions about limitations that we adapt around to get our jobs done. For example, you cannot define "no retro required" in a Type, it must be selected post-declaration, and when selected completely removes the ability to do a retrospective (even if you want to do a non-required one), not to mention it assumes this means you finished the incident and it will auto-archive the Slack channel. These are things we have to track cognitively instead of allowing the tool to keep the structure for us.
>
> For the rest of the time, `@_user3` and `@_user4` joined `@_user1` and `@user_2` in declaring incidents. Those of us who have done this a lot were there to guide and instruct when the person in the hot seat got stuck. The procedure went something like:
>
> 1. Spin the Wheel, get a *Function*. Not everything on the wheel was a named service.
> 2. Declare an incident from our new `#gamelan` Slack channel, where incident bot announcements are now configured to be sent.
> 3. Lookup the *Function* in the [Sorted Service Ownership](https://docs.google.com) sheet (which we also spent some time discussing, for instance we learned that one of our Services has ownership split between teams).
> 4. Identify what owner team should receive a page.
> 5. Switch to the new IR channel created by the incident bot and run through the process of paging the team using the bot, using a special dedicated Test service so all pages went directly to the facilitator (me) as a proxy. [Sidebar: using the PagerDuty integration through the bot actually failed silently on the first runthrough, but then worked fine for the next three. We still don't know what happened here, but this was a _failure in our production service_.]
>
> That's it. We assumed that whatever the circumstance, we had been called upon to declare the incident and page the team. We didn't go into assigning roles or anything else, this simple exercise prooved to be quite enough on its own.
>
> I have to say I loved `@user_2`'s turn, because we interrupted them at "life stuff" (grilling onions for lunch I believe?), a very real interruptive scenario for someone answering a call-to-action for an incident. She annoucned that first she would need to take time to take the onions off the stove and then could attend to the incident.
>
> I love these moments. But what I love more is seeing everyone there making discoveries and learning new things. Every time! One of my favorite aspects of doing these kinds of dives in PoPG is that we take the time to chat about what underlying processes are involved. We question why things are done how they're done, why work is being prescribed or imagined a certain way when we actually perform the work in a different way.
>
> So it's way beyond merely "how to use the product" and into critical discussions about our featureset, UX design, and integrations. For this reason, I wouldn't call this "on-the-job training" as much as I would call it practicing to work together. Which is what the Practice of Practice is all about.
>
> *-- Matt Davis, Autumn 2022*

{{<figure width=200 src="/2024/05/23/wheelofexpertise/wheel_no3.jpg" title="WoE the Many" alt="Wheel of Expertise, Fall 2022" >}}

# Reasoning

The **Wheel of Expertise** and its variants uncover opportunities for experts to share knowledge. It does this in a variety of ways:

1. Knowledge Elicitation spreads more understanding of the system to more people.
2. Sharing is done so that we witness real work, not just talk about hypotheticals.
3. Building reciprocity strengthens "we're all in it together", which can reduce anxiety.
4. Sharing mental models leads to synthesizing new patterns for recognition.
5. Building empathy between different company functions bridges context about priorities.
6. Humans learn exceptionally well when engaged in the act of play and discovery.
7. Assumptions are revealed while areas of little attention get examined.

Whether your exercise deploys a physical wheel or not, it is meant to be a catalyst for conversation. It is a useful way to break the ice and get people talking about things that they may not normally think about on a regular basis, or (even better) have opinions to share about how it works.

# Discussion

When I was first hired as an SRE (2013) and first played the game **Wheel of Misfortune** I was really excited about it. The general idea involves a wheel filled with incident ticket numbers, and the player must explain how they would go about dealing with the problem.

One of the big lessons I learned studying Resilience Engineering is that we're interested in what makes the system succeed just as much as we want to focus on failure. When I first heard this message it wasn't that difficult to wrap my head around it. I think I even said aloud in the class: "that's like when Miles Davis says there are no wrong notes in jazz."

We who run and make systems reliable are those jazz players, incidents are our unexpected jam sessions. But we are well-rehearsed together, so improvisation - or Adaptive Capacity - comes quickly to us. We are operating there at the "sharp-end" so we can apply direct therapy to support resilient operations.

The "sharp-end" is what the name implies: where instructions and controls issued by the "blunt-end" (i.e.: management or planners) are translated into actionable as-it-happens work. We all have "sharp-ends" when we work, regardless of our titles. They are the set of functions we know we can accomplish (and probably some we merely hope we can).

We don't actually know very much about what other "sharp-ends" look like, we're not doing that work, we can only imagine it. Getting to know each other's _actual_ Regular Work is helpful because it builds reciprocity and empathy, we get to know each other, and we learn where patches of Adaptive Capacity - our ability to improvise as a team - are nourished.

Often the only regular opportunities that bring these edges of work together are incidents. We're often very focussed on stopping the bleeding. There's also rarely room in a retrospective to get into the weeds, raise concerns, or ask probing questions about how we work. Learning Reviews get into this area, but they still require the right events that cover what it is we hope to learn.

Sharing in a dedicated, interactive setting like this forms strong bonds. We tend to recall information better when it is learned in a group setting, especially when it includes an element of fun. Some minds learn better when they can physically do the thing, coupling it with a visual experience or a particular place. And then in some cases like the storage bucket incident, an immediate return on investment is felt because of taking the proactive time to talk about our system.

Incidents and problems are not the only way to peer inside the complexity of sociotechnical systems. We can draw upon the same cognitive demands in other forums, outside of production pressure, without the atmosphere of an incident to burden us. The **Wheel of Expertise** uses interactivity to stimulate our curiosity in a group setting, which helps us share patterns between us, recompiling and integrating with our own dictionary for pattern recognition. This is a game that works especially well with participants from multiple areas of the company, because it strengthens intra-team bonds and emphasizes the work we do in coordination, collaboration, and communication.

# Epilogue

One final word on the Wheel and its conception.

This came at a time when we were working 100% remotely all across the globe while a pandemic raged. We needed innovative ways to remain connected as humans across video calls and chat channels. This motivated the kinds of interactive collaboration games I began inventing for us to play weekly.

At the same time, my wife Kary and I picked up the habit of watching **Good Mythical Morning** while cordoned in-place. At the end of each show, Rhett and Link spin the **Wheel of Mythicality** and play some kind of mini-game in the follow-up show, **Good Mythical More**. That's when I had the idea to see if I could find a wheel of my own to build a game I could play on Zoom calls with our SREs and people On-Call.

It is my version of a Wheel that can play _all_ the notes, regardless of whether they're wrong or not.

-- _Matt Davis, May 2024_
