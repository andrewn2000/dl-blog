# Setting up Gitblog - Part 2 Problems and Security

![](/images/2020-01-30/media/image1.png)

Comments on:[<span class="underline">https://www.fast.ai/2020/01/18/gitblog/</span>](https://www.fast.ai/2020/01/18/gitblog/)

Well its not so simple as just follow the instructions. Suppose you ALREADY have a domain name and its HOSTING mail for you. The problem is that if you yank the DNS, you’ll lose your mail and whatever other service you might like (ftp, webdav, etc) not just your web pages.

I’m hosted on Hostgator, but mine is a bit more complicated as I don’t have it hosting my registered names. For that I use a separate provider just in case one day I dislike Hostgator and move somewhere else.

If you’re just getting started, you might (and more likely will) find a registrar that has a special for $0.99 for one year. This means you can test it out for a year and see if you like their service and hopefully continue on as a customer. When I’m testing out ideas for websites, I use these special deals and point it to Hostgator. To me it makes more sense to use this and then when I near my anniversary date change it to my regular registrar should I want to keep the name or let it expire.

As the article suggested I change my nameservers to point to Github servers. Luckily my nameservers were rejected, which made me think a bit longer…as a failsafe. It’s always good to slow down when you encounter an error. Take a break or a walk.

I then went to Hostgator and looks at what I had there, and it looks like I’m supposed to remove the A record and then add the IPs from Github.

![](/images/2020-01-30/media/image2.png)

After that, everything “seemed” to work except the annoying “Not Secure”. Hmmm…

![](/images/2020-01-30/media/image3.png)

After googling a little bit, I found where you are supposed to be able to check the little box for “Enforce HTTPS” in the settings, but it was greyed out. Now mind you I had free SSL certs ALREADY installed so my site andynakamura.com had a certificate installed. Apparently, it didn’t like it when I changed the A record and wanted a new SSL. Ah, lesson learned. No problem, as I head over to zerossl.com and walk thru getting a new certificate installed on my webserver. By now, I’m a pro at this as the certs only give you 60 days.

Once I got my cert installed, I just had to wait a few hours and went to sleep. Like a little kid at Christmas, I woke up, went to the GitHub settings and selected the Enforce HTTPS and voila all was working\!

![](/images/2020-01-30/media/image4.png)

Now I can start getting this crazy blog going\! Onward\!
