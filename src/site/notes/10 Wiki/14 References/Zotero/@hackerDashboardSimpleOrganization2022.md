---
{"dg-publish":true,"permalink":"/10-wiki/14-references/zotero/hacker-dashboard-simple-organization2022/","tags":["wiki/references/article"]}
---

# Dashboard++ — a simple organization and navigation method for Obsidian Vaults
---
Dashboard++ is a method to organize and navigate through [[Obsidian\|Obsidian]] Vaults. It's an easy way to group notes into related topics and promote easy linking between notes and topics.

There's a [sample vault](https://github.com/TfTHacker/DashboardPlusPlus) to showcase Dashboard++.

![Pasted image 20230117145514.png](/img/user/90%20Meta/Attachments/Pasted/Pasted%20image%2020230117145514.png)

## How does it Work?
Dashboard++ is made up of two things:
- Custom [[CSS\|CSS]]
- [[Markdown\|Markdown]] lists

## Dashboard++ Structure
![Pasted image 20230117145705.png](/img/user/90%20Meta/Attachments/Pasted/Pasted%20image%2020230117145705.png)

## [[CSS\|CSS]] Snippet
```
/* Updated 2022-02-28 */

.dashboard {
    padding-left: 25px !important;
    padding-right: 25px !important;
    padding-top: 20px !important;
}

.dashboard .markdown-preview-section {
    max-width: 100%;
}

/* Title at top of the document */
.dashboard .markdown-preview-section .title {
    top: 60px;
    position: absolute;
    font-size: 26pt !important;
    font-weight: bolder;
    letter-spacing: 8px;
}

.dashboard h1 {
    border-bottom-style: dotted !important;
    border-width: 1px !important;
    padding-bottom: 3px !important;
}

.dashboard div > ul {
    list-style: none;
    display: flex;
    column-gap: 50px;
    flex-flow: row wrap;
}

.dashboard div > ul > li {
    min-width: 250px;
    width: 15%;
}
```

## Your First Dashboard
```
---
cssclass: dashboard
---
# Family
- 🏈 Sunday Game 
  - [[Spicy-Sweet Buffalo Popcorn]]
  - [[Guest list]] 
  - [Jalapeno Popper Wantons](https://www.allrecipes.com/166991)
- 👨‍👩‍👦 Objectives 
  - [[Family Recipes]] 
  - [[Family Calendar]] 
  - [[Education Plan]] 
  - [[Yearly Budget]]
- 🌅 Exotic Vacations  
  - [[Peru]] 
  - [[Austria]] 
  - [[Texas]]  
- 🎥 Movies to Watch 
  - [Sleepless in Seattle](https://www.imdb.com/title/tt0108160/) 
  - [Joe vs the Volcano](https://www.imdb.com/title/tt0099892/)
```

## Related Notes



###### META
Status:: #wiki/references/zotero/online
Related:: [[Obsidian\|Obsidian]]

Link:: https://tfthacker.substack.com/p/dashboard-a-simple-organization-and-navigation-method-for-obsidian-vaults-2b1982d023a0
ZoteroLink:: [@hackerDashboardSimpleOrganization2022](zotero://select/items/@hackerDashboardSimpleOrganization2022)
Author:: [[TfT Hacker\|TfT Hacker]]
Year:: 2022

Consumed:: true
Reconsume:: 
Rating:: 7
Priority:: 
Favorite:: 