---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Ranking College Football Coaches"
summary: "Using data science to evaluate recruiting and player development in college football"
authors: []
tags: ["Data Science"]
categories: ["Data Science"]
date: 2020-06-05T23:32:49-07:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "PC: CollegeFootballNews.com"
  focal_point: "Bottom"
  preview_only: false

  # Projects (optional).
  #   Associate this post with one or more of your projects.
  #   Simply enter your project's folder or file name without extension.
  #   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
  #   Otherwise, set `projects = []`.
  projects: []
---

{{< tabs tabTotal="2" tabID="1" tabName1="Overview" tabName2="Skills" >}}
{{< tab tabNum="1" >}}
#### Background<br>
I’m an avid college football fan with a keen interest in data science. For my first dive into data science, I will use some basic statistics and data manipulation to evaluate coaching in college football.
<br><br>

#### Defining the Problem</b><br>
Football is the crown jewel and breadwinner in any collegiate athletic department. A successful football program is not only a source of revenue for the university, it is also a powerful marketing tool, as studies have shown winning to be associated with increased donations, academic reputation, and lower acceptance rates. Therefore, it’s no surprise that coaches wield significant power and lofty salaries.

Coaches also carry the burden of high expectations, poor job security, and an average tenure of only 3.8 years. While the decision to hire or fire a coach is a multi-factorial process, it is primarily driven by their record. Consequently, a coach’s value, particularly with donors and fans, is inextricably tied to their performance on the field.

However, wins and losses are driven by several factors, many of which are outside a coach’s control, including conference affiliation, prestige, location, historical success, and financial investment from the university. As such, a coach’s record is not the most objective way to assess their value. In this project we will set out to define an approach for evaluating coaches while minimizing the impact of these confounding factors. Let's get started!

Continue reading on Medium: <a href="https://medium.com/@arsakhare87/using-data-science-to-evaluate-recruiting-and-player-development-in-college-football-a8c5c5cd447d"> Using Data Science to Evaluate Recruiting and Player Development in College Football </a>

Code can be downloaded at: <a href="https://github.com/arsakhar/NCAAF">https://github.com/arsakhar/NCAAF</a>

{{< /tab >}}

{{< tab tabNum="2" >}}
#### Technical Skills

<ol>
  <li>Data Visualization</li>
    <ul style="list-style-type:square;">
      <li>Histograms, scatterplots, qq plots, boxplots</li>
    </ul>
  <li>Data Scraping</li>
    <ul style="list-style-type:square;">
      <li>Scraping data across 4 different websites</li>
    </ul>
  <li>Data Cleaning</li>
    <ul style="list-style-type:square;">
      <li>Removing empty rows in dataframe</li>
      <li>Removing non-numeric / nan rows in dataframe</li>
      <li>Filtering dataframe by a specific keyword or attribute</li>
    </ul>
  <li>Data Manipulation</li>
    <ul style="list-style-type:square;">
      <li>Joining dataframes</li>
      <li>Transforming values on a dataframe column</li>
      <li>Applying a function elementwise on a dataframe column</li>
      <li>Filtering dataframe based on a specific attribute or keyword</li>
      <li>Aggregating on a dataframe column (standard deviation, mean, min, max, sum, count)</li>
    </ul>
  <li>Statistical Analysis</li>
    <ul style="list-style-type:square;">
      <li>Shapiro-Wilks test for normality</li>
      <li>Kruskal-Wallis non-parametric test for group differences</li>
      <li>Dunn post-hoc testing for pairwise comparisons</li>
      <li>Box-cox for transforming skewed distribution to a gaussian</li>
    </ul>
</ol>

#### Packages
<ol>
  <li>Beautiful Soup</li>
  <li>Scipy</li>
  <li>Matplotlib</li>
  <li>Pandas</li>
  <li>Numpy</li>
  <li>Scikit</li>
  <li>StatsModels</li>
</ol>

{{< /tab >}}
