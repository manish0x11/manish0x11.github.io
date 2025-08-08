---
layout: page
title: Notes
permalink: /notes/
---

# Counter from collections

while solving AoC-2024 day-1 part-2,my solution looks like below and when I asked ChatGPT for any other performance optimized solution,it suggest **Counter from collections module**

{% highlight python %}
# list1 = ['3', '4', '2', '1', '3', '3']
# list2 = ['4', '3', '5', '3', '9', '3']

similarity = [int(x)*list2.count(x) for x in list1]
print(sum(similarity))

# 31

# better way
list2_d = Counter(list2)

# list2_d = Counter({'3': 3, '4': 1, '5': 1, '9': 1})

similarity = [int(x)*list2_d[x] for x in list2]
print(similarity)
{% endhighlight %}

