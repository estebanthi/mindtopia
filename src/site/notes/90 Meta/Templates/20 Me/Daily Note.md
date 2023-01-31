---
{"dg-publish":true,"permalink":"/90-meta/templates/20-me/daily-note/"}
---

###### [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>\|↶ YESTERDAY]] ⁝ [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>\|TOMORROW ↷]]
# ◌ <% tp.date.now("dddd - MMMM Do YYYY") %>
---
## ↻ LOGS

## ✓ TASKS

###  ↑ TOP TASKS
```tasks
due before <% tp.date.now("YYYY-MM-DD",1, tp.file.title, "YYYY-MM-DD") %>
not done
priority is high
tags do not include tasks/habit
short mode
```

### ○ OTHER TASKS
```tasks
due before <% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>
not done
priority is below high
tags do not include tasks/habit
short mode
```

### ⚆ HABITS
```tasks
due before <% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>
not done
tags include tasks/habit
short mode
```

### ✓ COMPLETED TODAY
```tasks
done date is <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
tags do not include tasks/habit
short mode
```





###### META
Title:: 
Summary:: 


