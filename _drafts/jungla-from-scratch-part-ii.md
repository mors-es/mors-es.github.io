---
title: "JUNGLA from scratch [2]: Scenarios"
date: 2018-01-17 22:14:02.972000000 Z
tags:
- Startup
- Mobile App
- Design
description: "Define the features of the product"
---

> This serie of posts is an experimentation. I don't know _How to build a startup_. It's more a learning process, a documentation of all the steps we'll have to pass to test an idea.

Before drawing/coding anything the first think you have to be agree on is the _user journey_. This we help you to define the features of your product.

You can do it in many ways. We did it verbally, like a brainstorming. But at the end is really important to write down these scenarios so everybody is on the same wavelength (and it'll help to test the app later on).

One way to do it is to write _user stories_ like used in agile management. There are different syntax, as a developer I love the [Gherkin way](https://medium.com/@SteelKiwiDev/how-to-describe-user-stories-using-gherkin-language-8cffc6b888df).

Here the list of the features define with user stories:

```gherkin
Feature: Login
  In order to keep track of my journey on the app
  As user
  I want to be able to connect to the app with my Facebook login

  @login
  Scenario: Open the app the first time
    Given a new user
     When opening the app for the first time
      And clicking on the login with Facebook
     Then he arrive on the home page
```

```gherkin
Feature: Establishments
  In order to chose a nice place to go
  As user of Jungla
  I want to see a list of all the best establishments in Medellin on a map or on a list sort by categories

  @establishments
  Scenario Outline: Choosing a category
    Given a connect user
    And he is on the home page
    When is clicking on the <category>
    Then he see all the establishments in the category <category> on a map

    Examples:
      | category |
      | all      |
      | rumba    |
      | gourmet  |
      | culture  |
      | factory  |

  @establishments
  Scenario: Changing between map and list
    Given a connect user
    And he is on a category page
    And the view is a map
    When is clicking on the list button
    Then he see all the establishments on a list
```

```gherkin
Feature: Establishment
  In order to get information about an establishment
  As user of Jungla
  I want to see the detail of an establishment (events, pictures, offers, description, logo ...)

  @establishment
  Scenario Outline: Going to detail from index
    Given a connect user
    And he is on a category page with the view <view>
    When is clicking on <establishment> establishment
    Then he see the detail of the <establishment> establishment.

    Examples:
      | view | establishment |
      | map  | gora |
      | list |      |
```

```gherkin
Feature: Favorites
  In order to get keep track of my favorite places
  As user of Jungla
  I want to see select establishments as favorite

  @establishment
  Scenario Outline: Add an establishment in my favorites list
    Given a connect user
    And he is on a detail page of <establishment>
    When is clicking on the favorite button
    And going to the favorite page
    Then he see the <establishment> on the list

    Examples:
      | establishment |
      | gora          |

  @establishment
  Scenario Outline: Remove an establishment in my favorites list
    Given a connect user
    And he is on a detail page of <establishment>
    And the <establishment> is already favorited
    When is clicking on the favorite button
    And going to the favorite page
    Then he don't see the <establishment> on the list

    Examples:
      | establishment |
      | gora          |
```
