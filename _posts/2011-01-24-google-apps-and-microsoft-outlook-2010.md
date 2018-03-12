---
title: Google Apps and Microsoft Outlook 2010
date: 2011-01-24 00:15:43.000000000 -08:00
category: blog
tag:
- personal
- web
- GMail
- Google
- Google Apps
- Microsoft
- Outlook
---
<p>With the need to save money, I finally decided to take the plunge and try out Google Apps after a strong recommendation from a friend. Getting everything converted was simple enough, I just had to sign up for a Google Apps account, add my domain and away I go.</p>
<p>For those interested, when you search for Google Apps, Google will always bring you by default to their Google Apps for Business edition first. It is a bit of a maze to find the standard Google Apps, but it is <a href="http://www.google.com/apps/intl/en/group/index.html">there</a>.</p>
<p>The main difference between the two is that you get 7GB of space instead of 25GB. Other minor stuff include Google Video, forced SSL and 99.9% uptime SLA. For that, you have to pay $50 <strong>per user</strong> per year. This is as opposed to getting 50 free users for your domain, not including any aliases you would like to use (known as nicknames in Google Apps). Another stated difference is that you are unable to sync with Microsoft Outlook and Blackberry Phones etc. This, however, I have been able to prove to be incorrect.</p>
<p>I have been able to sync up my Outlook and Blackberry through IMAP. True, it is not exactly like Exchange and you lose certain functionality - such as notes and journal. However, I would like to argue that overall, for someone or a company with less than 50 users, Google Apps is more than enough.</p>
<p>One thing to note though, the setup instructions that are available on Google's site is incorrect. The following IMAP settings worked for me:</p>
<p><code><br />
Username: user@yourdomain.com<br />
Password: your password<br />
IMAP: imap.googlemail.com<br />
IMAP Port: 993<br />
Encryption: SSL<br />
SMTP: smtp.googlemail.com<br />
SMTP Port: 587<br />
Encryption: TLS<br />
</code></p>
<p>One other thing that I did do was to <a href="https://www.google.com/accounts/UnlockCaptcha?">Unlock Captcha</a>. Not sure if it is related, but I did this before I found the above settings so I can not comment if it was either due to the settings or both changes were required.</p>
<p>I will give this a go for a week or two before I fully terminate my old Exchange account. As always... hope this helps and remember to have fun!</p>
