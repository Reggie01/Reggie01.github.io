---
layout: post
title: Day 5: Flex Panels Image Gallery | Javascript30
category: Javascript30
tags: js, html, css
description: Review Javascript30 Day 5: Flex Panels Image Gallery
image: https://images.unsplash.com/photo-1504066116688-57c2efd91274?auto=format&fit=crop&w=1500&q=80
date: 2018-01
---

>The doors we open and close each day decide the lives we live. -Flora Whittemore

## Current Mission
Day 5: Flex Panels Image Gallery challenge is to create transitions when panels are clicked on.
  
## Set up initial look of webpage
In this challenge we first need to set up the page.
  1. The panel elements need to display vertically and not horizontally. We can solve this by changing the display on our panels.
  {{code}}
  .panels {
      ...
      display: flex;
    }
  {{/code}}
  2. The panel needs to expand in size when clicked on. To achieve this effect we need to add
  {{code}}
  flex-grow : #number
  {{/code}}
### Add Event Listeners, Paragraph Transitions
    
### Issues
 
 
#### Optional Reading Material 
 
Have A Good Day!!


Headline Blog

Outline Blog
1. Set up initial look of webpage
  (Parent) display: flex
  (Child)   flex-grow : #number
  P elements : first and second child need to be displayed off viewport
2. Add transitions and onclick events
  panels - each panel needs an onclick events
  onclick each panel should expand. 1st and 3rd paragraphs should translate into viewport
