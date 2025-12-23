---
layout: post
title: "Weird Talks"
---

Having done hundred of interviews at various levels, they're not always smooth, and some situations have happened are so comically bad that I have to share them.

# Small Tech Company

I was passed onto a very early technical screen with a smaller company. After appying and doing a quick HR screen, I was doing a live coding screen with a manager in less than 3 days. We introduce ourselves, have some initial banter, then jump into the leetcode problem. Everything is normal until I have some misunderstandings about the problem, then we start talking through it.

> **Me:** Hmm, I know what I want to do but I can't remember the exact syntax.
> **Interviewer:** Go ahead and Google it then, I think that's realistic enough.
> **Me:** Oh okay, let me check.
> **Interviewer:** Just to make sure, you're googling X right?
> **Me:** Yeah, just because I wasnt to do this specific thing.
> **Interviewer:** Oh, actually let's ignore that, I'd like you to implement it yourself.
> **Me:** Sure? I guess I can, but real world I wouldn't roll my own.
> **Interviewer:** True, but I want to see what you'd do since you already know what you're trying to do.

A bit strange, but we worked together to get a shared understanding, then things took a turn. Since they were still working during my interview they got paged about an incident. I undertand it's tough to get dedicated time, and the power dynamics of a candidate and HM are skewed, but it was setting a bad tone. I continued to talk through the problem, and they continued with ignoring me, asking me to repeat myself, and overall just not paying attention. Thankfully I didn't get a follow up technical loop.

# Major Tech Company

The initial steps were normal, HR screen, resume walk, HM talk, technical screen, then continuation to the final loop. The technical screen was a leetcode style assessment which was expected and I felt I did about 75% on. I was told I passed and scheduled the final loop which was a troubleshooting portion, past projects, then HM chat to close it out. I've done my best to recall the dialog as it happened for the first troubleshooting portion:

## First Troubleshooting

> **Interviwer 01:** You support X service, you get a page that the site is down, what is your next step?
> **Me:** I go to our website via a browser to see if the site is still up.
> **Interviewer 01:** Why would you do that?
> **Me:** To see if it's a false alarm or not.
> **Interviewer 01:** You don't have to do that. The alarm fired, I need you talk about what troubleshooting steps you're taking.
> **Me:** Okay. Am I able to SSH to the machine remotely.
> **Interviewer 01:** Why are you trying to remotely connect to the machine?
> **Me:** I want to verify I still have connectivity since we're not abl-
> **Interviewer 01:** You don't need to check connectivity, what does the alarm say?
> **Me:** You said I was paged that the service was down.
> **Interviewer 01:** Right, so what do you do?
> **Me:** Ah, so what is the alarm paging about?
> **Interviewer 01:** Actually, it's multiple alarms firing.
> **Me:** Oh. What alarms are firing?

I was belittled by the interviewer as my intelligence was questioned for the entirety of the troubleshooting portion. I understand that not everyone who is the interviewer is an expert about the question they're asking, and that they're trained to leave breadcrumbs, but the impression I got from this interviewer was that their main goal was to test my patience.

## First Past Projects

The past projects was new to me. Another interviewer asked me about my resume and my past work, and delved into the technical details about them. Below is my recollection of our chat:

> **Interviewer 02:** So I see you worked on a secrets-comparator tool.
> **Me:** Yes, we have a bunch of non-prodduction enviornments and configuration drift was causing a lot of pain for us.
> **Interviewer 02:** Why didn't you just have a vault with all the secrets?
> **Me:** I did ask about that, but they recently migrated to their current infrastructure set up.
> **Interviewer 02:** So you didn't want to make a different tool to use a vault system?
> **Me:** I think it'd solve a lot of problems, but I only made this tool initially to solve some upfro-
> **Interviewer 02:** I get it, but a vault system is better.
> **Me:** Yeah it is.
> **Interviewer 02:** So when will you ask about changing from your tool to a vault system?
> **Me:** Well the tool I made is a stop gap until we can bet-
> **Interviewer 02:** Do you not want to migrate to a vault system?

This was how our conversation went for the rest of this part of the call. I could see why they were hung up on me not making immedate architectural changes instead of solving immediate pain points first. But again, it felt like this portion of the interview was just to test my patience more than anything.

## Coding Portion

The coding portion was bad from the start. We do our introductions, then the interviewer turns off their camera, mutes their mic, and sends a link to the leetcode assessment. They unmute, talk about the problem, then go back to being muted.

> **Interviewer 03:** Hey, please look at the problem and solve it.
> **Me:** Okay let me take a look.
> **Me:** Hmm, my initial impression it to solve it in this manner. Let me try some initial psudo code.
> **Me:** Okay so to talk through why I-
> **Interviewer 03:** You don't have to talk, just tell me when you're done.
> **Me:** Oh okay.
> **Me:** Alright now I'm ready to talk about where I'm at now.
> **Interviewer 03:** This doesn't look like a complete solution.
> **Me:** Yes, I'm a bit stumped so I wanted to talk through this together.
> **Interviewer 03:** There's no need to discuss anything, you can keep working.

After a while I also muted myself and turned off my camera and typed a bit. They unmuted to see if solved the problem, but I was already upset with how I was being treated and talked through gritted teeth.

## First HM Chat

The HM portion was a nice break. They asked about how the loop went, I said "I felt alright, but we won't know till they decide". We talked more about the position and such, but since we talked before this was more of a formality. They did ask a soft pitch behvior question to fill the time, then we ended the call.

About a week later I get a call directly from the HM saying that based on the interview feedback they wanted to down level me. I said that's fine, just let me know what the steps are to continue with the process. They said they'd close the initial position I applied for, then send me the listing for the new position to apply to.

This had a smell to it since any large tech company that talks about down levels is able to do it without another application. Regardless I applied again, worked with the same recruiter who's aware of all of this, and I'm scheduled for another final loop (troubleshooting, projects, HM). The troubleshooting portion was tweaked to be coding related i.e. what's wrong with this code. Below is how I remember it:

## Second Troubleshooting

> **Interviewer 04:** So there is an issue with this code.
> **Me:** Can I run it first to see what it does.
> **Interviewer 04:** It doesn't run.
> **Me:** Due to the error or due to the enviornment?
> **Interviewer 04:** Maybe you should read through the code first.
> **Me:** Oh, this portion looks wrong, and this part seems syntatically incorrect.
> **Interviewer 04:** What do you mean?
> **Me:** <Explains the bug>
> **Interviewer 04:** Right, but how would that present if you ran this code?
> **Me:** We talked about running the code first, is that still an option?
> **Interviewer 04:** Well now it is, but do you know why?

Again, my intelligence attacked, the interviewer uninterested in having an interactive discussion, and instead focusing on why I'm not following their opaque logic. We talk a bit more about the fix, then move onto reimplementing it i.e. a leetcode problem. Here's how that went:

> **Me:** Well I think I'd start like this.
> **Interviewer 04:** You sure? That doesn't look right.
> **Me:** Yeah, I'm just trying to get some thoughts out first, so this is my first pass.
> **Interviewer 04:** I don't think that's still right though.
> **Me:** Oh okay, let me just focus on psudo code then we can see if my thinking makes sense.
> **Interviewer 04:** Why are you doing psudo code?
> **Me:** Just so I can explain my thought process before we get-
> **Interviewer 04:** I'm not sure what you're trying to explain, don't you see the problem?
> **Me:** Well, it's not apparent to me right-
> **Interviewer 04:** Come on, it's right there, you should get this easily.

I think they had the solution in front of them they couldn't grasp that I wasn't getting it. Which means their own training about how to conduct a technical interview wasn't up to par either, so they failed me in that capacity.

## Second Past Projects

Since this position was downleveled, there wasn't a coding portion, and instead went straight into the past projects. To my surprise I had the same interviewer from when I did my first past projects. Once we got through our introduction I metioned this fact and the conversation changed.

> **Interviewer 02:** We've talked before?
> **Me:** Yes, we talked about my secrets tool.
> **Interviewer 02:** Hmm, give me a second.
> **Me:** Okay.
> **Interviewer 02:** I'm asking HR if we still need to do this portion since we've done it before.
> **Interviewer 02:** Okay they said you're good.
> **Me:** Huh?
> **Interviewer 02:** I've interviewed you before so you're good.
> **Me:** Oh, do I pass?
> **Interviewer 02:** Yup, no worries.
> **Me:** Thanks! This was my easiest pass.

I wasn't sure what else to do except take their 'pass' at face value. It still rubbed me that I got the same person less then 2 weeks apart and they didn't remember me. It just showed to me how disorganized their process was behind the scenes.

## Second HM Chat

I had another final HM chat with a soft pitch behavioral question, chop it up, then end the call. Overall this loop felt about the same as the other, but in the end I didn't get an offer.

Part of me thinks it wasn't so much my perfomance but because they might've violated some internal policy or process by having me reapply instead of keeping me internal. Even though the HM wanted to get their replacement hired, I don't think the team was ready (or wanted) to bring on someone new.

# Aerospace Company

After applying for a position, I was set up with a call to do my initial HR screen and resume walk. Everything was fine until I was ambushed.

> **Interviewer:** So because the position is technical, the HM has a few question we like to ask.
> **Me:** Okay sure.
> **Interviewer:** So imagine you're deloying an application to a cluste, why would it fail?
> **Me:** Uh, it could be a lot of things? Is there enough resources? Do we have observability into the health of the cluster.
> **Interviewer:** Yes, but why do you think it fails?
> **Me:** Hmm, a misconfiguration, there's a lot of reasons I think.
> **Interviewer:** Actually the HM was looking for 'the cluster reached capacity which causes new deployments to fail since no new artifact storage unavailable'
> **Me:** Oh, okay yeah that could be a reason too.

They asked 3 other trivia-esq questions and told me answers that weren't technically wrong, but a normal person wouldn't have been able to get to on their own. And a technical interviewer wouldn't be able to coach someone to the answer without a longer conversation, not just 4 questions over 10 minutes.

Thinking back to it, this might've been some kind of code-word for hiring their own pre-vetted candidates. Whether the HR rep was complicit or ignorant isn't clear though.