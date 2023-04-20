---
title: HOMEPAGE
date created: 2023-04-20
date modified: 2023-04-20
---

![[近期计划]]

# 最近编辑的笔记

```dataview
table WITHOUT ID file.link AS "标题",file.mtime as "时间"
from ""
sort file.mtime desc
limit 10
```


# 最新创建的笔记

```dataview
table file.ctime as 创建时间
from ""
sort file.ctime desc
limit 10
```

![[宏观数据]]