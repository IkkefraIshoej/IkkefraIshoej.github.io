---
layout: custom
title: My First Post
---

<div class="post-content">
<h1> New york crashes </h1>
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
    <img src="/assets/factor.png" alt="My Image">
    <div class="text-container">
      <p>The plot shows that most of the crashes are labeled as unspecified, therefore this category will be removed to get a clearer view of the distribution of the crashes that actually has a category. </p>
    </div>
  </div>
  
</div>

<style>
body {
  background: linear-gradient(to right, #212946, #A267F5);
  margin: 0;
  padding: 0;
}

.post-content {
  margin: 0 auto;
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
}

.image-container {
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: center; /* Center images horizontally */
  width: 100%; /* Make the image container full width */
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

