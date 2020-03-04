---
layout: post
title:  "Cryptopals Set 1 Challenge 1"
date:   2020-02-19 12:30:48 -0800
---

I decided to use Python to do the Cryptopals challenges the first time around. Working with raw bytes becomes fairly simple with Python3.

The first cryptopals challenge is to convert `hex` to `base64`. My aim with Cryptopals was to use these challenges to really learn concepts that I otherwise would've brushed aside.
With this challenges, I decided to learn about the different encodings out there, especially `unicode`.
 

{% highlight python %}
hex_value = "49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d"
raw_bytes = bytes.fromhex(hex_value)
expected_base64_string = "SSdtIGtpbGxpbmcgeW91ciBicmFpbiBsaWtlIGEgcG9pc29ub3VzIG11c2hyb29t"
assert to_string(base64.standard_b64encode(raw_bytes)) == expected_base64_string
{% endhighlight %}

