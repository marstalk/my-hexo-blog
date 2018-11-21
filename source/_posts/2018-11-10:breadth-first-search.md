---
title: breadth-first-search
date: 2018-11-10 15:36:52
tags:
---
完整的py3代码如下：
```
from collections import deque

# about this demo:
# 广度优先搜索的例子，基本思路：
# 维护一个队列，待搜索队列，
# 1，从队列中取出一个元素。
# 2，如果这个节点是正在寻求的结果，那么结束
#    否则，将这个节点的邻居放到队列中
# 3，重复这三个步骤，直到将整个队列为空。

# init test data
graph = {}
graph["you"] = ["alice", "bob", "claire"]
graph["alice"] = ["peggy"]
graph["bob"] = ["peggy", "anuj"]
graph["claire"] = ["jony", "thom"]
graph["peggy"] = []
graph["jony"] = []
graph["anuj"] = []
graph["thom"] = []
# end init test data


def check(name):
    return name[-1] == "m"


def breath_search(name):
    search_que = deque()
    search_que += graph[name]
    while search_que:
        tem_people = search_que.popleft()
        if check(tem_people):
            return tem_people
        search_que += graph[tem_people]
    return None


print(breath_search("you"))

```
