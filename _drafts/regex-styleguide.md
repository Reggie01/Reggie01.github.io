---
title: Useful Regex for Style Guide
category: regex
tags: regex
---

Useful Regex for Style Guide
==========
Lately, I am in the process of implementing style guides to my html, css, and js files. I started initially just making changes by brute force to css and html files. Now that I'm on js files I've decided to embrace the DRY principle with some regex. The following is my first attempt at adding spaces to all parentheses.
<code>
  /* Just  parentheses */
  pattern = (?:\()([\']?\w+[\']?)(?:\))
  replace = \( $1 \)
  
  /* parentheses or brackets */
  pattern = (?:\[[\s]?)(.+)(?:[\s]?\])
  replace = \[ $1 \]
  
  /* parens */
  pattern = (?:\{+)\s+(\w+\:?\s?\#?\w+\;)\s+(?:\}+)
  replace = \{ \1 \}
</code>
Some examples of patterns that the regex will capture i.e 
<code>
  [blue]
  [ "blue" ]
  [ {} [] ]

  ["bar"]
  [[ "foo" ]]
  [foo[ i ]]
  [[1] 1]
  [123, 123, 245, 456]
  [{foo: { bar: "foo"}]
  [{color: "purple"}]
  [ windSpeeds[ i ] ]
</code>
I'm using this pattern to match all code between parentheses. Then replace with a space between the match and parentheses. The bracket pattern I'm using to match anything within a bracket. Then add space between the match and bracket. Do not just copy and paste the regex. Make sure that you double check that it suits your particular purpose. A possible site to test your code is (regexr.com)[http://www.regexr.com/].