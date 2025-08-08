---
layout: page
title: Notes
permalink: /notes/
---

## Counter from `collections`

While solving **AoC 2024 – Day 1, Part 2**, my initial solution was:

{% highlight python %}
list1 = ['3', '4', '2', '1', '3', '3']
list2 = ['4', '3', '5', '3', '9', '3']


similarity = [int(x) * list2.count(x) for x in list1]
print(sum(similarity))  # 31
{% endhighlight %}


When I asked ChatGPT for a performance-optimized version, it suggested using the **Counter** class from the **collections** module:

{% highlight python %}
from collections import Counter

list2_counts = Counter(list2)  # {'3': 3, '4': 1, '5': 1, '9': 1}
similarity = [int(x) * list2_counts[x] for x in list1]
print(sum(similarity))  # 31
{% endhighlight %}


