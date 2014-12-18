---
title: Introduction to Probability Theory
layout: default
---

# Introduction to Probability Theory

Normally, when working with statistics, we use high-level concepts like "distribution", "sampling", "null-" and "alternative hypothesis", etc. And in most cases it is enough to understand a subject. Sometimes, however, to grasp some method or relation, we need to dive deeper in terminology and basic notation. This post is about the very core of probability theory that everybody should know to understand and treat statistical methods correctly.

## Experiment / Trial

Everything starts with an **experiment**. Normally experiment is thought of as a repeated procedure performed by a human, but in broader sense it can also refer to any act of observing world's phenomena or occurrences. For example, tossing a coin, looking at a traffic light or checking today's weather - all of these are examples of experiments. Sometimes we also work with composed experiments, consisting of fixed number of "sub-experiments" (like individual coin tosses). These "sub-experiments" are commonly referred to as "**trials**".

## Outcomes and random variables

The goal of experiment is to get an **outcome**. For coin tosses, for example, there are 2 possible outcomes - "heads" and "tails", and for weather it may be "sunny", "raining", "snowy", etc. All possible outcomes form so-called **sample space**, which we will denote as [Omega] (read as "big omega"). 

Outcomes don't have to be simple values like "heads", but in fact can be complex objects. For example, if we establish social experiment and ask causal people on the street to take a survey, each of these people will be considered as an outcome. In this settings, data provided by these people (e.g. their height, gender, profession, etc.) may be considered as **random variables**. 

Strictly speaking, random variable (or simply r.v.) is a _function_ of an outcome, that describes its particular property. In social experiment, for example, r.v. [height(person)] maps values from set $People$ to a set of real numbers [R], while r.v. [profession(person)] maps same values to a fixed set [Professions]. 

<table align="center">
  <tr>
    <td><img src="{{ site.url }}/assets/fry.gif" style="height:300px"></td>
    <td>
      $X_1 = gender(Fry) = male$<br/>
      $X_2 = height(Fry) = 171$<br/>
      $X_3 = weight(Fry) = 68$<br/>
      $X_4 = age(Fry) = 1029$<br/>
      $X_5 = profession(Fry) = delivery \: boy$<br/>
    </td>
  </tr>
</table>

In practise, however, random variables are rarely written in a function notation, but instead capital letters with optional indexes (e.g. [X_1] or [Y]) are normally used. Values, that these random variables may take, are written in lower case (e.g. [X=x] means that r.v. [X] got value [x] in a described experiment). 
Note, that notation for random variables may comflict with notation for sets, but in most cases it doesn't cause confusion. 

## Events

## Probability and its distribution

- probability space

Independent variables

Dependent variables and conditional probability

... 

[P(X=x)] denotes aggregative probability of all outcomes in which r.v. [X] has the value [x]. 



-- Into to Stats

Population and sample (+ sampling itself)

Expectation and variance

