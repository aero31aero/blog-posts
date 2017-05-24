# Zulip Summer of Code
I would be interning at Zulip in the summers of 2017, and it has been pretty eventful already. So here's a brief of how I started contributing to Zulip and what I plan to work on.

## Finding Zulip
It all began in October when my friend and WikiToLearn hacker [Srijan Agarwal](https://github.com/Srijancse) invited me to try contributing to a live editor for WikiToLearn. I had been trying unsuccessfully to get the developer environment for WikiToLearn up and running but failng to that for quite some time because of some dependency issues when I finally decided to give up on it. Also worth noting is that MediaWiki being a PHP application was a factor. I know people do serious work in PHP but I can't get myself to do that for some reason.

I was one day searchng for alternatives to Slack for a group chat application because, well, Telegram isn't too good for large groups. That was when I stumbled onto Zulip. Finding out that they were a part of GSoC last year was a huge plus and that's when I decided to give this a try.

I was thrilled to see Zulip Dev Environment working on the first go. It was the programmer equivalent of *next...next...install* and there it was, a Vagrant container running Ubuntu 14.04 with all the dependencies installed and the Django plus Tornado application running. My first patch was pretty stupid in retrospect, but there's always a first time. I didn't know how to run tests, I didn't even know how to test the code changes I made. It was messy, and [Tim Abbott](https://github.com/timabbott), Org Admin for Zulip, helped me out there.

## Mistake

This was where I made my mistake on the road to GSoC. I wasn't yet sure if I wanted to focus on Zulip and it was just my first patch and it received a few comments. Cool, I made the changes Tim asked, and waited. In the meantime I stumbled around thinking of trying to go back to MediaWiki or maybe trying my hands on Qt. My patch wasn't yet merged and I saw other people's patches getting accepted so I was giving up hope on Zulip. 23 days later, I got this message from Tim before he merged my PR:
> @aero31aero it looks like you forgot to post a comment when you updated your PR, so I didn't look back at this until now.

Basically, I'd lost out 23 days of time that I instead might have spent on Zulip fulltime. I went back and started interacting with the community again, and this time I communicated more than earlier, picking up minor issues and looking for potential project ideas. I got intrested in the bots and integrations that Zulip had and started wishing there was a way to use them easily like with Telegram Bots. That was how I got the idea for my GSoC Proposal.

## GSoC Proposal

To sum in one line, this was my idea: *Automated Deployment of Zulip Bots*. Here's the abstract I wrote:

>With this project, I aim to simplify the process of bot creation and running, and make it as smooth as possible by adding the following features:
- Easy Deployment from GitHub to Heroku
- Configuration Generator for bots using external services
- Package management for bots
- Basic API permissions management dashboard
My main aim is to decouple the bots from Zulip's core (zulip/zulip repository) and make the bot discovery and installation process easier for users.

I was getting positive feedback from the community and from my friends who were also preparing their own proposals and I continued sending patches as well as revising my proposal as the days went by. Then came the waiting period at the end of which I found out I wasn't selected. Needless to say, self-confidence goes down when you've been trying hard to achieve something and fail. I contacted Tim to know what I did wrong and instead got the good news that I was instead short listed for the unofficial internship program that Zulip offers: Zulip Summer of Code.

## Zulip Summer of Code

Since the ZSoC results came 2 weeks after GSoC results, I had already made some plans for after my college exams and thus went on a small trek just after the college exams. Luckily, my mentor, [Deigo Berrocal](https://github.com/CestDiego), was also a little busy that first week and starting today, that is, 24th May, 2017, I'll begin working for Zulip.

I am part of the Integrations Team along with circa 10 other people including mentors and interns. We would be holding weekly work distribution and discussion meetings, followed by regular work done the regular Zulip way. Tonight would be the second meeting and the first where I pick up some work. Looking forward to spending the summer working on integrations in Zulip. Keep you all posted.