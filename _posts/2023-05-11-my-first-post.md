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
    <img src="/assets/years2.png" alt="My Image">
    <div class="text-container">
      <p>This is some text next to the second image.</p>
    </div>
  </div>
  
  <p>This is some text below the images.</p>
  
</div>

<style>
  body {
    background: linear-gradient(to right, #212946, #A267F5);
  }
  
  .post-content {
    margin: 0 auto;
    max-width: 70%;
    background-color: #212946;
    padding: 20px;
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 26px;
  }
  
  .image-container {
    margin-top: 20px;
    display: flex; /* Use flexbox layout */
    align-items: center; /* Vertically center elements */
  }
  
  .text-container {
    margin-left: 20px; /* Add some space between image and text */
  }
</style>
