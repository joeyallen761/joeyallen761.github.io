---
title: "Hello world"
layout: archive
title: "Basketball Shot Trainer App"
permalink: /project/project1
author_profile: true
image: "/images/Projects/BasketballAppScreenshots/icon.jpg"
---

This is a project that employs a medley of huggingface models, speech-to-text, time-series analysis, visualization, and LLM prompt engineering to provide feedback to a basketball player as they practice their shot.

## Motivation
I have long been interested in how computer vision can mesh with biomechanics for various purposes, from creating interactive art displays to improving sport performance, rehabilitation, wildlife tracking, and more. I made this project to get experience working with frameworks relevant to this line of work.

## The Data
All good AI projects need to start with data. There are many more data sources I could have collected, but my aim was to make something that other people would be able to use on themselves with minimal budget and setup.

At the end of the day, I wanted to collect biomechanical data for each shot, and a label that determined where the ball ended up: "make" or "miss". If I did miss, I wanted to record which direction the ball missed to. 

So, I devised a plan to capture this: I went to the gym and put on some headphones. I set up my phone camera to record myself shooting freethrows, and set the video to capture audio from my headphones instead of the phone. Then, I got in front of the camera and started shooting freethrows. After each shot, I said aloud either "make", "left", "right", "short", or "long".

After collecting sufficient data, it was time to make it useful.

## Extracting Pose Information from Video

My first data-wrangling goal was to extract a useful represention of biomechanic "pose" data for basketball shooting sessions. I researched many APIs to achieve this task, and ultimately decided to choose DeepLabCut because their API will work on huggingface models for non-human animal research also, and I am interested in doing that in the future. After a brief wrestling match with installation and pathing issues, I got my small laptop to succesfully run this software on a small proof-of-concept 30-second video of myself shooting exactly 3 free throws.

<p align="center">
  <img src="../images/Projects/BasketballAppScreenshots/labeledscreenshot.png" alt="My second photo" width="400"/><br/>
  <em>This is a visualization of DeepLabCut's output as I shot a freethrow.</em>
</p>

For larger videos down the line, I turned to Google Colab for compute resources.

### Section 2.1: Interpreting Pose Information

DLC is nice bc output is well formatted
filtering noisy data
indexing uncertainty


<!-- <div class="img-with-caption"> -->
  <!-- <iframe src="../images/Projects/BasketballAppScreenshots/Plotly/autoencoder_4sec_offline.html">
  </iframe> -->
  
  <iframe src="../images/Projects/BasketballAppScreenshots/Plotly/autoencoder_4sec_offline.html"
        width="100%" height="600" style="border:none;"></iframe>

<!-- </div> -->

  <iframe src="../images/Projects/BasketballAppScreenshots/Plotly/autoencoder_4sec_standalone.html"
        width="100%" height="600" style="border:none;"></iframe>


browsing huggingface models - google colab
The text continues
<div class="img-with-caption">
  <img src="../images/Projects/BasketballAppScreenshots/all_joint_positions_shot1.png" alt="All joints position during shot 1"/>
  <em>This graph shows the tracked Y-positions of all major joints throughout shot 1, labeled as a right-side shot.</em>
</div>

<div class="img-with-caption">
  <img src="../images/Projects/BasketballAppScreenshots/wristposition.png" alt="Wrist position during shot 3"/>
  <em>Trajectory of both wrists and the forehead for a single shot, highlighting coordinated movement during release.</em>
</div>

<div class="img-with-caption">
  <img src="../images/Projects/BasketballAppScreenshots/wrist_movement_threeshots.png" alt="Wrist movement over three shots"/>
  <em>Side-by-side visualization of the wrist movement over three full shot attempts, with body keypoints overlaid.</em>
</div>

<div class="img-with-caption">
  <img src="../images/Projects/BasketballAppScreenshots/session_report.png" alt="Session averages bar chart"/>
  <em>Summary chart showing shot outcome frequencies across an entire session, with a strong majority of makes.</em>
</div>

<div class="img-with-caption-wide">
  <img src="../images/Projects/BasketballAppScreenshots/openai_feedback.png" alt="Text feedback summary"/>
  <em>Text-based feedback generated after the session, including insights and improvement tips based on performance data.</em>
</div>

<div class="img-with-caption">
  <img src="../images/Projects/BasketballAppScreenshots/labeledscreenshot.png" alt="Pose tracking during freethrow"/>
  <em>This is a visualization of DeepLabCut's output as I shot a freethrow.</em>
</div>

<div class="img-with-caption">
  <img src="../images/Projects/BasketballAppScreenshots/data_filtering.png" alt="Filtered vs raw wrist movement"/>
  <em>Comparison of raw and smoothed wrist position data to highlight the benefit of applying filtering techniques.</em>
</div>