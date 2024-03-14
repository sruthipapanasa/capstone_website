---
title: Developing Political Personas Through Generative Language Modeling
---

<link rel="stylesheet" type="text/css" href="style.css">

<button><a href="#Introduction">Introduction</a></button>
<button><a href="#Objectives">Objectives</a></button>
<button><a href="#Methods">Methods</a></button>
<button><a href="#Results">Results</a></button>
<button><a href="#Limitations">Limitations</a></button>
<button><a href="#RelatedW">Related Works</a></button>
<button><a href="#Next">Next Steps</a></button>
<button><a href="#Meet">Meet the Team</a></button>


## Introduction
<p id="Introduction">
  <span class="new-line">The main goal of politicians is to cater to their constituents and understand the changes they want to see. To do so, they need to be able to accurately identify their target voters, contact and survey them, understand their values and ideals, and predict which policies would best represent such populations. However, this process can often be time-consuming and expensive. Our project aims to help this problem. </span>
  
  <span style="margin-top: 20px;" class="new-line">Twitter data contains a wealth of information that contains public opinions on policies and politicians. By analyzing tweets from different political groups, we aim to create personas that mimic key voter groups using LangChain Agents and OpenAI’s GPT-3.5 Turbo API. Our goal is to develop a model that can generate new data to predict real voting patterns based on previously posted tweets. We will then be able to ask these personas different political questions and explore their response and reasoning. </span>
</p>

## Objectives
<p id="Objectives">
  <span class="new-line"><strong>Locate a Political Candidate’s Target Audience:</strong>
  Because our model can predict public opinion on political issues, candidates can figure out which voters align best with their policies in order to accurately target their campaign’s marketing efforts, which will help voters feel better represented by their leaders.</span>
    
  <span style="margin-top: 20px;" class="new-line"><strong>Forecast Success of Political Candidates’ Policies:</strong>
  Candidates can ask our model to predict whether the exact policies they want to implement will gain favor or discontent from the public. They can use these responses to tailor their policies that will represent and benefit as many voters as possible.</span>


  <span style="margin-top: 20px;" class="new-line"><strong>Address Limitations of Surveys and Cold Calling:</strong>
  Surveys and cold calling are very time-consuming and expensive. These traditional methods also have a low success rate as the average person may not take time out of their day to complete them. Our project addresses this problem.</span>

</p>

## Methods
<p id="Methods">
  <span class="new-line"><strong>Part 1: NLP Approach - Sentiment Analysis</strong></span>
  <ol>
    <li>Calculated the average sentiment of each user’s tweets and classified each user into Biden-supporting voter, Trump-supporting voter, or neutral voter</li>
    <li>Split the Biden-supporting users into Biden Strong and Biden Weak based on a sentiment threshold, repeated for Trump-supporting users</li>
  </ol>

  <span style="margin-top: 20px;" class="new-line"><strong>Part 2: LLM Approach - Model Development</strong></span>
  <ol>
    <li>Used LangChain as our model integration framework and OpenAI’s GPT-3.5 Turbo-Instruct API to create an LLM-powered generative model that can use trained clusters to produce the political affiliation, policy related opinions, opinion polarity, and emotional tone relating to common political discourses of 5 select voter populations</li>
    <li>Created 5 models, named Biden_strong, Biden_weak, Neutral, Trump_strong, Trump_weak</li>
    <li>Model training:
      <div>
          <span class="new-line"> - <em>Semantic training</em>: analyzes the training tweets’ semantic language style and word choice to extract the tone and emotion of select voter type </span>
          <span class="new-line"> - <em>Contextual training</em>: uses author’s tone description and analyzes the context and meaning of training tweets to extract the political stance, candidate affiliation, and general opinion of voter type </span>
      </div>
    </li>
    <li>Asked the five models 9 questions about relevant political topics (e.g. gun control, abortion legalization, climate change, etc.) and recorded results to gain understanding of sample political opinions</li>
  </ol>

  <div>
    <p><strong>Flowchart of Methods</strong></p>
    <img src="flowchart.png" alt="Flowchart of Methods">
  </div>
</p>

## Results
<p id="Results">
  <span class="new-line"><strong>NLP Findings</strong></span>
  <ul>
    <li>1,260 users: 645 support Biden (51%), 461 support Trump (37%), 154 are neutral (12%)</li>
    <li>The sentiment score results are strongly negative, meaning it is more common for users to express support for a certain candidate by expressing negative views about the competing candidate, as opposed to positive views about their own</li>
  </ul>

  <span class="new-line"><strong>LLM Findings</strong></span>
    <ul>
      <li>Outputs for models were very emotionally charged, polarizing, and made use of strongly opinionated language</li>
      <li>Even neutral model expressed its moderate views with strong conviction</li>
      <li>Result aligns with our initial expectations, as Twitter contains the most intense opinions, and this is reflected by our model</li>
    </ul>
</p>

## Limitations
<p id="Limitations">
  <ul>
    <li>Open AI API limits how many tweets we can sample due to exceeding the number of tokens available</li>
    <li>Datasets have limited data and it’s very skewed towards tweets with negative sentiments (not enough tweets with positive sentiments)</li>
    <li>Datasets are only available for Trump and Biden, thus limiting our insight about other parties such as the Independent party, Green party, etc.</li>
    <li>Only data from 2020’s tweets are used, so the current political climate is not accurately reflected</li>
  </ul>
</p>

## Next Steps
<p id="Next"> 
  <ul>
    <li>Be able to feed our models the latest Twitter data to get a more accurate picture of the current political climate</li>
    <li>Find a way to sample more Tweets than we can with the limitation of our current model</li>
    <li>Have our model output more streamlined answers through prompt engineering so that further analysis can be performed on the model responses</li>
  </ul>
</p>

## Related Works
<p id="RelatedW">
 <strong>Using Sentiment Analysis to Define Twitter Political Users' Classes and Their Homophily During the 2016 American Presidential Election</strong> by Caetano et al.
  <br>
  <a href="https://jisajournal.springeropen.com/articles/10.1186/s13174-018-0089-0#Sec3" class="button">Click Here for the Article</a>
  <!--<div>
    <a href="https://jisajournal.springeropen.com/articles/10.1186/s13174-018-0089-0#Sec3" class="button">Click Here for the Article</a>
  </div> -->
  <span class="new-line"><strong>AI-Augmented Surveys: Leveraging Large Language Models and Surveys for Opinion Prediction</strong> by Junsol Kim and Byungkyu Lee </span>
  <!--<div>
    <a href="https://arxiv.org/abs/2305.09620" class="button">Click for the Article</a> 
  </div> -->
</p>

## Meet the Team
<p id="Meet">
  <div class="gallery">
    <div>
        <img src="vivian.jpg" alt="Vivian Lin">
        <p>Vivian Lin</p>
        <a href="https://www.linkedin.com/in/vivian-esther-lin/" class="button">LinkedIn</a>
    </div>
    <!--<div>
        <img src="tonoya.jpg" alt="Tonoya Ahmed">
        <p>Tonoya Ahmed</p>
        <a href="..." class="button">LinkedIn</a>
    </div> -->
    <div>
        <img src="sruthip.png" alt="Sruthi Papanasa">
        <p>Sruthi Papanasa</p>
        <a href="https://www.linkedin.com/in/sruthi-papanasa/" class="button">LinkedIn</a>
    </div>
   <!-- <div>
        <img src="anna.png" alt="Anna Liu">
        <p>Anna Liu</p>
        <a href="https://www.linkedin.com/in/annaliu2/" class="button">LinkedIn</a>
    </div> -->
  </div>
</p>
