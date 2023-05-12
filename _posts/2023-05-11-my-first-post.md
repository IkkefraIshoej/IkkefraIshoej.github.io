---
layout: custom
title: Final project 
---

<div class="post-content">
<h1> New york vehicle crashes </h1>
<h3> A visualization story </h3>

  <p>The aim of this visualization story is to give readers an overview of crashes in Manhatten - NYC - from 2013-2022. Furthermore, we have also created a machine learning model that tries to predict wheter or not a person has been injured or killed in a crash. The usecase for this could be to register data and then alert nearby emergency rooms with a warning when a crash occurs. 

 The data is gathered from NYC open data platform and is based on the first responders initial gathering of data. We supplied that data with weather data from the local stations for each day represented in the dataset, and with information about the road lengths on which the crashes occurs. First, a plot of the crashes over the years is shown.</p>
  
  <div class="image-container">
    <img src="/assets/years.png" alt="My Image">
    <div class="text-container">
      <p>It is easy to see that the crashes are more or less constant over the years, with two exceptions. In 2016 the crashes dropped significantly in April, and then COVID-19 hit in March 2020, leading to many fewer crashes, which has continued in the previous two years. The next thing to look for is the distribution of reasons for crashes.</p>
    </div>
  </div>


  <div class="image-container">
    <img src="/assets/weathercrash.png" alt="My Image">
    <div class="text-container">
      <p>From this plot , it is easy to see the peak temperature of causing crashes is around 23 degree, basically summertime. It is reasonable to tell the truth with higher temperature, people are less patient. This could be a potential reason to increase the risk of vehicle crash.</p>
    </div>
  </div>

<div class="image-container">
    <img src="/assets/weatherinjured.png" alt="My Image">
  </div>
  <div class="image-container">
    <img src="/assets/weatherdeath.png" alt="My Image">
  </div>
  <div class="text-container">
    <p>Regarding the injuries and deaths numbers related to the vehicle crashes, overall the numbers of injuries is dramatically higher than the deaths. The numbers of motorist injured have the highest number among the three different weather conditions, which are 'Clear', 'Rain' and 'Snow'. The numbers of pedestrians injured ranked second, and the third place goes to the number of motorist injured.</p>
  </div>

<div class="image-container">
    <img src="/assets/neighbourbar.png" alt="My Image">
    <div class="text-container">
      <p>When we take a look into the vehicle crash frequency by neighbourhood, we can figured out from the plot that the neighbourhood'Midtown-Midtown South' has the highest crash rate with more than 35000 crashes in total. The second highest neighbourhood is 'Hudson Yards-Chelsea-Flatiron-Union Square' covering approximately 28500 crashes. The third places goes to the neighbourhood 'SoHo-TriBeCa-Civic Center-Little Italy', the crash number roughly around 22500. The lowest crash rate neighbourhood is 'Stuyvesant Town-Cooper Village', only has about 1500 crash in total. The gap betwwen the hightest and the lowest is really huge.</p>
    </div>
  </div>


  <div class="image-container">
    <img src="/assets/factor.png" alt="My Image">
    <div class="text-container">
      <p>The plot shows that most of the crashes are labeled as unspecified, therefore this category will be removed to get a clearer view of the distribution of the crashes that actually has a category. </p>
    </div>
  </div>

<div class="text-container">
      <p>The plot below shows the distribution for the top 14 factors over the years from 2013-2022. It is clear that some of the categories were removed over the years. We can see that turning improperly went down, and that all factors took a natural big drop during the covid years, with the exception of drivers disregarding traffic control, that seems to be steady throughout the years.  </p>
</div>
 <div class="image-container">
    <img src="/assets/factoryear.png" alt="My Image">
</div>

<div class="text-container">
      <p>The next plot shows the distribution for each of the focus factors throughout the 168 hours of the week. The most interessting takeaway from the plots are that the traffic control disregarded seems to be high on all hours of the week, meaning it is more comon for that to occur during the night than most of the other categories. We can also see that passing too closely goes down in the weekend, which might be because people are not as much in a hurry as they are on weekdays. Almost all of the categories peak on friday afternoon, probably because people want to go home.   </p>
</div>
 <div class="image-container">
    <img src="/assets/168hours.png" alt="My Image">
</div>

<div class="text-container">
      <p>Next we want to explore the distribution of crashes troughout the different areas of manhatten for each factor. The plot shows that particularily the neighbourhood West Village, alot of the categories peak. This might be due to to the fact that the other areas sets the factor as unspecified, or simply that the area needs to apply changes for it to be more safe. In general there are less counts of crashes for almost all categories in the north of Manhatten. </p>
</div>
 <div class="image-container">
    <img src="/assets/maps.png" alt="My Image">
</div>

<div class="text-container">
      <p>We wanted to look how rain affects the number of casualties. So this plot shows the crashes with casualties when it rains as the purple heatmap, and the red dots as the crashes with casualties when it does not rain </p>
</div>

{% include rainmap.html %} 

<div class="text-container">
      <p>A machine learning model was created, hoping that we could try to predict wheter or not a person was injured or killed in a crash. Application for this could be a warning system for the nearest emergency room, as they would be better prepared when an accident happens in their area. The first step was to examine the correlation between the variables in the dataset, and the result can be seen in the correlation matrix below. The variable does not correlate much, so the hopes for the model wasn't much. We decided to go with a randomforrestclassifier, and a variable indicating if a person was either injured or killed in the crash was added.
 </p>
</div>

 <div class="image-container">
    <img src="/assets/correlation.png" alt="My Image">
</div>

<div class="text-container">
      <p> The resulting model had an accuracy of 86%, and the confusion matrix shows the results that we had on the test set, which was 30% of the data. Not an impressive model result, but it was able to classify some of the crashes that had injuries or fatalities the right way.
 </p>
</div>

 <div class="image-container">
    <img src="/assets/confusion.png" alt="My Image">
</div>
<div class="text-container">
      <p> Lastly we also wanted to include how the Alchohol involvement factor looked over the years, surprisingly there are not many records in the dataset where alcohol was the leading factor. The animation below shows the location of the vehicle crashes over the years on Manhatten. There doesn't seem to be a specific place where the alchohol incidents occur, but as there are over 2000 bars in manhatten,  that would also be surprising.
 </p>
</div>

{% include vehicle_crashes_map.html %} 

<div class="text-container">
<h3> Conclusion </h3>
      <p> Our extensive analysis of the causes, trends, and geographic distribution of automobile collisions in Nyc from 2013 through 2022 offered valuable insights. Over the years, we noticed a steady crash rate with a vastly disproportionate number of injuries to fatalities. The main reasons for collisions have changed over time, and some areas, such West Village, have had a higher rate of collisions. Rain in particular emerged as a sophisticated element affecting collision fatalities. Though it requires more work, our machine learning approach showed promise in terms of forecasting crash outcomes. Although there are relatively few accidents involving alcohol, their serious repercussions cannot be disregarded. The importance of data analysis and predictive modeling in boosting traffic safety and planning efficient emergency responses is highlighted by this study.

 </p>
</div>



</div>

<style>
body {
  background: linear-gradient(to right, #212946, #A267F5);
  margin: 0;
  padding: 0;
}

.post-content {
  margin: 20px auto;
  max-width: 80%;
  background-color: #212946;
  padding: 20px;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 26px; /* Reduce the font size */
  box-sizing: border-box;
  overflow: hidden; /* Hide horizontal scrollbars */
  border-radius: 25px;
}

.image-container {
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: center; /* Center images horizontally */
  width: auto; /* Make the image container full width */
}

.text-container {
  margin: 0 20px;
  text-align: justify; /* Justify the text */
}

img {
  max-width: 70%; /* Make images responsive */
  height: auto;
}
</style>

