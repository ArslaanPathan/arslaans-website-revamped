---
layout: post
title: "Age verification in Systemd"
author: Arslaan Pathan
image: /assets/images/post-image/systemd-age-verification.png
---

Recently, the systemd project has merged Pull Request #40954, introducing a `birthDate` field to the userdb JSON.  
You might be asking, "Why is this bad?" or "What does this mean?", and as there is a lot of misinformation out there, it may be hard to get a clear answer on this topic.  

This blog post aims to explain it clearly in words even a non-techie person can understand.

## The issue

To give some context for the non-techies, systemd is a core part of most Linux systems. It manages most of the apps that run in the background that are needed for your computer to work. While there are alternatives to systemd, almost all distros use it, and once it's on your computer (it usually comes preinstalled), it's incredibly difficult to take its "digital tentacles" out of your system.

Recently, systemd merged a pull request ([#40954](https://github.com/systemd/systemd/pull/40954){:target="_blank"}) to add a `birthDate` field to userdb from systemd-homed.  
In simple terms, systemd added support for tracking the user's birth date inside of the users database, in response to the new laws requiring operating systems to verify the ages of users in California (AB-1043), Brazil (Lei 15.211), and Colorado (SB26-051).

## Why this is controversial

This pull request being merged has caused much controversy in the FOSS community as of recent times. Many people believe that this violates the "free" and "libre" nature of Linux, and that there was no need for systemd to do this. 

Although the systemd project claims it is an 'optional field' and that it will 'not be required for use', it's starting to become a lot less optional than we thought.  
GNOME, a popular desktop environment for Linux (in simple terms, the desktop of your computer) is starting to rely a lot more on the new `birthDate` field to the point that it might be required to use GNOME.  
Along with this, xdg-desktop-portal (in simple terms, the file picker/screenshare manager) is working on adding an age verification portal that integrates directly with the new systemd `birthDate` field.

The more insane part of this actually comes from where the PR (pull request. simple definition: a snippet/addition of code written by someone else requested to be added to the mainstream codebase) came from. The creator of the PR, `dylanmtaylor`, stated himself that this field was, and I quote, "hilariously pointless and ineffective" at verifying anyone's age, then continued to push for it to be merged into the codebase anyway. Even more ironic? The people who merged the PR into the mainstream codebase were engineers at Microsoft. Microsoft, of all companies. The company that makes the piece of spyware we call "Windows 11".

## My take

I'll be honest for a minute.

Yes, it's an 'optional' field. And yes, systemd didn't write the laws that started this all in the first place. But that doesn't make this okay.

Systemd has NO right storing your birthdate at all. It's an init system. While yes, systemd-homed stores PII (Personally Identifiable Information) like full names, that's in relation to user accounts, not an init system. This also ties into another problem with systemd that's been discussed for ages: scope creep. The fact that systemd, an init system, made to manage background services, now has infrastructure for age verification? That's an example of systemd expanding its scope into places it shouldn't even need to be. Network connections? Somehow that's systemd's job? DNS resolver? That's... also systemd's job somehow, despite better tools existing like dnsmasq? And now it's got infrastructure for AGE VERIFICATION??

Putting the scope creep aside, let's be real. As a 13-year-old, even I was taught in primary school that rule #1 of the internet is "DO NOT SHARE YOUR PERSONAL INFORMATION." And yet, now we have the same companies and organisations and lawmakers who told us not to share our information merely 13 years ago asking us to share our IDs, videos of ourselves, our names, phone numbers, hell, at this point Google probably knows your Social Security Number.

The cherry on top? The PR was merged by Microsoft engineers. The same company that built Windows 11, an operating system that treats you less like a user and more like a product. An operating system that spies on your every move and forces their Microsoft accounts and other spyware onto you (ahem, Windows Recall).  
Make of that what you will.

If you care about Linux staying free,  
If you care about Linux staying libre,  
If you care about digital sovereignty,  
Pay attention to this one.

---

### Sources

- [https://ostechnix.com/systemd-userdb-birthdate-age-verification/](https://ostechnix.com/systemd-userdb-birthdate-age-verification/){:target="_blank"}
- [https://itsfoss.com/news/systemd-age-verification/](https://itsfoss.com/news/systemd-age-verification/){:target="_blank"}
- [https://news.ycombinator.com/item?id=47436240](https://news.ycombinator.com/item?id=47436240){:target="_blank"}
- [https://www.sambent.com/the-engineer-who-tried-to-put-age-verification-into-linux-5/](https://www.sambent.com/the-engineer-who-tried-to-put-age-verification-into-linux-5/){:target="_blank"}
- [https://agelesslinux.org/distros.html](https://agelesslinux.org/distros.html){:target="_blank"}
- [https://linuxiac.com/systemd-introduces-birth-date-support-for-upcoming-linux-desktop-age-controls/](https://linuxiac.com/systemd-introduces-birth-date-support-for-upcoming-linux-desktop-age-controls/){:target="_blank"}
- [https://github.com/systemd/systemd/pull/40954](https://github.com/systemd/systemd/pull/40954){:target="_blank"}
