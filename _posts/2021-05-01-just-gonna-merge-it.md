---
layout: post
title: "Just Gonna Merge It"
---

In a previous software job, I was asked to integrate work from a previous team. Due to the complexity of the system, it'd boil down to reading a diff of every changed file, then copy-pasting the lines of code over as needed. 

At the time I was also crowned our team's 'Git Guru' since I understood it the best our of our entire team. And by understood it I mean I knew the difference between fetch and pull. I didn't keep the information to myself and explained a lot of git concepts at length with team members. But I also spent a lot of time back seat driving, at their request, to make sure they made a new branch correctly.

Looking at the completion date of the previous team's work, it was less than 6 months old. Our project's release cycle was measured in quarters, and we hadn't had a release in over 9 months. Comparing the changed files, the delta was simple and less than ~100 LoC.

Using git I checked out the branch for each feature, merged it into my own testing branch of the next release candidate, then validated that the builds and tests passed.

I did the same thing for the remaining branches and finished a task that was estimated to be 2 months in 2 week. Even then, most of the time was spent on the build process (around 2 hours) and setting up the tests (build had to be walked over and booted in the test environment).

While catching up with a former team member after I left the company, they confessed that our team lead didn't believe I did all the work and asked if I got help from any one else. In retrospect I could see why they'd be skeptical. The experience showed me that by having more than a working knowledge of your tools, you can make mundane tasks disappear almost entirely.