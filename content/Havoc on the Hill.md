---
title: Havoc on the Hill
draft: True
---

In January 2023, I set out to determine how much work Canadian politicians actually do. Since the government's job is to pass bills, I figured the [LEGISinfo](https://www.parl.ca/legisinfo/en/overview) database would be a good place to start. After downloading some data files and writing a quick web scraper with [Beautiful Soup](https://pypi.org/project/beautifulsoup4/), I had all the data I could possibly need. Then, I used [pandas](https://pandas.pydata.org/) to analyze the data and [plotly](https://plotly.com/) to create some charts.

>[!remark]+ Remark
>In hindsight, I don't know why I didn't use matplotlib for plotting. I've been using it for my research this summer, and its so much faster and more intuitive than plotly. The one benefit of plotly is that you can create interactive HTML charts, but I didn't use that feature. Oh well, you live and you learn.

Anyways, here's what I found in seven simple plots. I hope you find it interesting. If you want to view my messy two year old source code, its available on my [github](https://github.com/rileywheadon/canadian-legislation-visualisation).

## Part 1: Making the Bills

![[bills-by-type.png]]

![[bills-by-party.png]]

## Part 2: Reading the Bills

 A productive government should get around to reading all the bills that are proposed. Whether the government actually passes these bills is more nuanced, but at the very least I would hope the government is reading a couple of bills a day. So here's another plot, which shows the bill readings per day in the past 17 sessions of the house of commons.

![[readings-per-day.png]]

As you can see, Stephen Harper's minority conservative government between 2007 and 2010 appeared to be reading the most bills. Justin Trudeau's majority government was far less efficient, reading less than half of the number of bills per day. Overall, the productivity of parliament, measured by bill readings, seems to be on a downward trend since the early Harper era.

I also imagine that a productive government would either pass or reject the bills in a reasonable amount of time. This can be measured with *deliberation time*, or the length of time between the first and last readings of the bill. If a bill is rejected upon the first reading, its deliberation time will be $0$. However, the deliberation time remains a useful metric for the bills that make it past the first reading, since the majority of these bills are eventually passed (see below). Therefore, the median deliberation time can also be viewed as a proxy for a government's bill-passing speed.

![[deliberation-time-pm.png]]

From the above plot, it appears that the median deliberation time was approximately constant across the past four prime ministers. That being said, the 75th percentile was *noticeably* higher for the two more recent governments, especially Justin Trudeau. This could mean that modern governments are attempting to pass more bill simultaneously, resulting in a higher number of active bills at one time and thus longer deliberation times.

![[deliberation-time.png]]

The above plot contains a distribution the of all deliberation times in the dataset. As mentioned previously, many bills have short deliberation times of less than 50 days, likely the ones that are rejected. However, the majority of bills are either passed or rejected after 200 days, and almost all bills are passed or rejected after a year.

## Part 3: Passing the Bills

![[bills-by-stage.png]]

![[bills-per-day.png]]

## Conclusion
