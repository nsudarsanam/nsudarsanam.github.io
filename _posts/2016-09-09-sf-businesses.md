---
layout: drama
title: "What happened to the economy of San Francisco?"
date: 2016-09-09
---

One of the enduring stories of San Francisco is the journey the city has taken through its businesses. This city has seen fortunes rise and fall periodically across multiple neighborhoods within multiple types of businesses in those neighborhoods.<br>
Having lived in the city only for 9 years but yet having seen so much flux in the character of its businesses, I wanted to try to answer the following questions: when did these changes start, can we classify them and which neighborhoods have experienced the brunt of them?

<h3> <b> How? </b></h3>
The <a href="https://data.sfgov.org/Economy-and-Community/Registered-Business-Locations-San-Francisco/g8m3-pdis">registered business database </a> contains the tree rings that traces the changing economy of the city starting from 1959. <br>
The data has 5 major columns: start and end dates of businesses as well as their physical locations along with their industry class.

<hr>

<h3> <b> The 20-ft view: </b></h3>
<figure>
<img src="/images/2016-09-09/timeline.png">
<figcaption> Number of businesses changing over time from 1960-2016 </figcaption>
</figure>
Grouping by the various dates, I found that San Francisco went through 3 significant peaks of economic activity followed by corresponding dips. The highs were in 1968, 2006 and 2014 and the dips were in 1969, 2007 and 2015. <br>
This view answered the first of my questions: 2014 was the peak of all the change in the city. And that was the period I’d have to dig into.

<hr>

<h3> <b> The 10-ft view: </b></h3>
Now, I wanted to answer what classes of businesses were most active during this period? Considering only businesses that opened post-2012 and were still operational, I first grouped the data by the physical coordinates of the businesses and then by their industry.

<figure>
<img src="/images/2016-09-09/open_by_industry.png">
<figcaption>New businesses opened post-2012 grouped by industry</figcaption>
</figure>

Unsurprisingly, construction and rental services figured in the top 5 but the more pedestrian sounding categories of “Transportation and warehousing” and “Accommodations” also appeared, which seemed quite odd.
<br>
<br>
To answer the final question, I broke the same data down by neighborhood.

<figure>
<img src="/images/2016-09-09/open_by_industry_hood.png">
<figcaption>New businesses opened post-2012 grouped by industry and then by neighborhood</figcaption>
</figure>

And this led to a strange revelation.<br>
Sunset/Parkside topped the list with the most businesses within the Transportation category. Also, traditionally neglected neighborhoods of
Excelsior and Bayview/Hunters Point bubbled to the top with the same category. The category of Accommodations also figured heavily in this list.<br>
So what did these categories really mean?

<hr>
<h3> <b> The 5-ft view: </b></h3>
Looking at specific examples of businesses with these classifications led me to believe that these businesses were predominantly people registering their uber/Lyft gigs or their airbnb-ed apartments! That led to an interesting
idea where it now might be possible to identify which neighborhood produced the most uber drivers and where were most of the airbnb apartments located?

<i> Where does your uber driver come from? </i> <br>
I considered all businesses with the classification of Transportation and that had either the words “uber” or “lyft” in their business name.<a href="#caveat1"><i>*</i></a>

<figure>
<img src="/images/2016-09-09/new_drivers_over_years.png">
<figcaption>Total count of Uber/Lyft driver registrations over the years</figcaption>
</figure>

Last year marked an enormous spike in uber driver registrations. <br>
To find their origins, I then grouped this data by neighborhood and plotted the top 6.

<figure>
<img src="/images/2016-09-09/drivers_per_hood.png">
<figcaption>Number of Uber/Lyft registrations per neighborhood over the years</figcaption>
</figure>

That revealed an interesting pattern. Mostly middle/lower-middle class neighborhoods topped this list. Sunset/Excelsior/Bayview all showed significant growth of uber drivers over the years.<br> <br>
That made me curious about which neighborhoods produced the fewest drivers.

<figure>
<img src="/images/2016-09-09/drivers_bottom_per_hood.png">
<figcaption>Least number of Uber/Lyft registrations per neighborhood over the years</figcaption>
</figure>

<i>Which is the most Airbnb-ed neighborhood?</i> <br>
Trying to isolate Airbnbs from all the businesses within the “Accommodations” category proved to be a tricky proposition. Probably due to ever-changing legislation around short-term rentals, people were more circumspect when registering their Airbnbs. There were far fewer businesses with the words “airbnb” or “bnb”. <br>
So instead, I tried eliminating obvious businesses with a whitelist that contained words like “hotel” or “motel” or “apartments” and further refined the list by eliminating anything that sounded like a business (containing words like “corp”,”trust”).<a href="#caveat2"><i>**</i></a>


<figure>
<img src="/images/2016-09-09/total_airbnb.png">
<figcaption>Total number of Airbnb registrations over the years</figcaption>
</figure>

2014–2015 proved to be the height of short-term rental registrations in the city. I then broke the count down by neighborhood.

<figure>
<img src="/images/2016-09-09/airbnb_per_hood.png">
<figcaption>Number of Airbnb registrations by neighborhood over the years</figcaption>
</figure>

The contrast between the neighborhoods featured here versus those in the ride-sharing case was quite stark. These neighborhoods had decidedly higher incomes. My only rationalization is that maintaining and renting out an apartment takes some investment. In contrast, ride-sharing services have a lower barrier to entry requiring just a car (which in some cases the services themselves subsidize).<br><br>

This led me to a startling conclusion:<br>
<b>the Ubers and Lyfts of the world do more for the lower-middle class sections of a city unlike Airbnb, the latter targeting middle-upper middle class of a city.</b><br>

Finally, the neighborhoods with the least number of Airbnbs were either extremely well to-do or poor.


<figure>
<img src="/images/2016-09-09/bottom_airbnb_per_hood.png">
<figcaption>Neighborhoods with the least number of Airbnb registrations over the years</figcaption>
</figure>

<hr>
<h3> <b> In summary: </b></h3>
This project taught me that the journey of exploring data can lead you to unexpected places. It takes relationship building with the dataset,a getting-to-know-each-other period eventually resulting in answering questions that might have been different from what you started with. <br>
The story of businesses in San Francisco is so much more rich and I’ve only scraped the surface. For example, this data could illuminate where are  most business owners located (are they out-of-state investors or local owners?). Which industries were the most adversely affected post-2012? Which neighborhoods saw the most business closures?

<br><br>
<a name="caveat1"><i>*</i></a>: The Uber/Lyft registration count is a lower-bound, since its possible people have registered their businesses under other aliases.<br>
<a name="caveat2"><i>**</i></a>: The Airbnb registration count is also a lower-bound since its possible that we’ve eliminated legitimate airbnbs that have been registered by businesses and not individuals.