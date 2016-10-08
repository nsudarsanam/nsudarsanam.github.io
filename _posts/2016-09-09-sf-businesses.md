---
layout: drama
title: "Is my neighbor is airbnb-ing their apartment?"
date: 2016-09-09
---

The question of short-term rentals has been hugely contentious in the city of San Francisco for the past few years.
Having lived in the city only for 9 years but yet having seen so much flux in the character of its neighborhoods, I wanted to try to answer two questions: <b>which neighborhood produces the most uber drivers and what are the odds my neighbor is airbnb-ing their apartment?</b>

<hr> 

<h3> <b> How? </b></h3>
The city has opened up their <a href="https://data.sfgov.org/Economy-and-Community/Registered-Business-Locations-San-Francisco/g8m3-pdis">registered business database </a> that contains information for all registered businesses starting from 1959. <br>
It has 5 major columns: start and end dates of businesses, their physical locations and their industry class defined by <a href="https://www.naics.com/naics-drilldown-table/">NAICS codes.</a><br>
<hr class="section-divider">

<h3> <b> What year should I be even looking at? </b></h3>

To isolate the period that made most sense to investigate, I grouped the data by various dates.
<figure>
<img src="/images/2016-09-09/timeline.png">
<figcaption> Number of businesses changing over time from 1960-2016 </figcaption>
</figure>
 It turns out that San Francisco experienced 3 significant peaks of economic activity followed by corresponding dips. The highs were in 1968, 2006 and 2014 and the dips were in 1969, 2007 and 2015. <br>
So, most of the recent change was contained in the years of 2014-2015.
<hr>

<h3><b>How do I find those businesses that represent ride-sharing drivers and airbnbs?</b></h3>
This is where the NAICS code helped greatly. Looking at only those businesses that opened post-2012 and were still operational, I first grouped the data by the physical coordinates of the businesses and then by their NAICS code.

<figure>
<img src="/images/2016-09-09/open_by_industry.png">
<figcaption>New businesses opened post-2012 grouped by industry</figcaption>
</figure>

It turns out that the pedestrian sounding categories of <i>Transportation and warehousing</i> and <i>Accommodations</i> topped the list. Less surprising, were the categories of <i>Construction</i> and <i>Rental Services</i> figuring in the top 5. 
<br>
<br>
To find which neighborhoods had higher concentration of these industries, I grouped the same data by their neighborhoods.

<figure>
<img src="/images/2016-09-09/open_by_industry_hood.png">
<figcaption>New businesses opened post-2012 grouped by industry and then by neighborhood</figcaption>
</figure>

And this led to a strange revelation!<br>
Sunset/Parkside, a traditionally more middle-class neighborhood of the city topped the list with the most businesses within the <i>Transportation</i> category. Also, the poorer neighborhoods of Excelsior and Bayview/Hunters Point bubbled to the top with that same category.<br>


<hr>
<h3> <b> So, where does your uber driver come from? </b></h3>
I focused on businesses of type <i>Transportation</i> and that contained the words “uber” or “lyft” in their business name<a href="#caveat1"><i>*</i></a> and counted them up across the years.

<figure>
<img src="/images/2016-09-09/new_drivers_over_years_city.png">
<figcaption>Total count of Uber/Lyft driver registrations over the years</figcaption>
</figure>

Last year marked an enormous spike in the number of ride-sharing driver registrations. <br>
To find their locations, I then grouped this data by neighborhood and plotted the top 6.

<figure>
<img src="/images/2016-09-09/drivers_per_hood.png">
<figcaption>Number of Uber/Lyft registrations per neighborhood over the years</figcaption>
</figure>

That revealed an interesting pattern. Mostly middle/lower-middle class neighborhoods topped this list. Sunset/Excelsior/Bayview all showed significant growth of uber drivers over the years.<br> <br>
That also made me curious about which neighborhoods produced the fewest drivers.

<figure>
<img src="/images/2016-09-09/drivers_bottom_per_hood.png">
<figcaption>Least number of Uber/Lyft registrations per neighborhood over the years</figcaption>
</figure>

 In contrast, these neighborhoods were characterized by much higher incomes. 

<hr>
<h3> <b> What are the chances your neighbor is airbnb-ing their apartment? </b></h3>
Trying to isolate Airbnbs from all the businesses within the <i>Accommodations</i> category proved to be tricky. Due to ever-changing legislation around short-term rentals, people were more circumspect when registering their Airbnbs. There were far fewer businesses with the words “airbnb” or “bnb”. <br>
Instead, I tried eliminating commercial businesses with a list that contained words like “hotel” or “motel” or “apartments” and further refined the list by eliminating anything that sounded like a business (containing words like “corp”,”trust”).<a href="#caveat2"><i>**</i></a>I then counted the businesses left-over across the years.


<figure>
<img src="/images/2016-09-09/total_airbnb.png">
<figcaption>Total number of Airbnb registrations over the years</figcaption>
</figure>

2014–2015 proved to be the height of short-term rental registrations in the city. I then broke the count down by neighborhood.

<figure>
<img src="/images/2016-09-09/airbnb_per_hood.png">
<figcaption>Number of Airbnb registrations by neighborhood over the years</figcaption>
</figure>

The contrast between the neighborhoods featured here versus those in the ride-sharing case was quite stark. These neighborhoods had decidedly higher incomes. This can be due to the fact that maintaining and renting out an apartment takes some investment. In contrast, ride-sharing services have a lower barrier to entry requiring just a car (which in some cases the services themselves subsidize).<br><br>

This led me to a surprising conclusion:<br>
<b>the ride-sharing apps of the world do more for the lower middle-middle class sections of the economy unlike Airbnb, the latter targeting middle-upper middle class of the economy.</b><br> 
Finally, (similar to the ride-sharing case) neighborhoods with the least number of Airbnbs were either extremely well to-do or poor.


<figure>
<img src="/images/2016-09-09/bottom_airbnb_per_hood.png">
<figcaption>Neighborhoods with the least number of Airbnb registrations over the years</figcaption>
</figure>

<hr>
<h3> <b>What's next? </b></h3>
I had initially begun this project to find the neighborhoods that have been through the most change. But I got waylaid by a different question along the way, that of the impact of the gig economy on our city.<br>
So, the journey of exploring data can lead you to unexpected places. It takes relationship building with the dataset,a getting-to-know-each-other period eventually posing questions that might have been different from what you started with. <br>
I also recognized the infinite possiblities of this data. For example, this dataset could reveal where most business owners are located (are they out-of-state investors or local owners?). Which industries were the most adversely affected post-2012? Which neighborhoods saw the most business closures? The story of businesses in San Francisco is rich and ever-changing. This project has only scratched the surface.

<hr>  

<a name="caveat1"><i>*</i></a>: The Uber/Lyft registration count is a low ball estimate, since its possible people have registered their businesses under other aliases.<br>
<a name="caveat2"><i>**</i></a>: The Airbnb registration count is also a low ball estimate since its possible that we’ve eliminated legitimate airbnbs that have been registered by businesses and not individuals.