---
{"dg-publish":true,"permalink":"/004-workbench/90-meta/templates/wiki-note-public/"}
---

```
<%* 
const fileName = await tp.system.prompt("File Name");
const fileType = await tp.system.suggester(["Embryo", "Germinating", "Mature", "Rejuvenated", "Withered", "Plantation"], ["embryo", "germinating", "mature", "rejuvenated", "withered", "plantation"]);
const dateNow = tp.date.now("YYYYMMDDhhmmss");
const fullFileName = fileName + " - " + dateNow;
await tp.file.rename(fullFileName);
const wikiPath = "004 Workbench/10 Wiki";
const inboxPath = wikiPath + "/11 Wiki Inbox";
const notesPath = wikiPath + "/12 Notes";
const plantationsPath = wikiPath + "/13 Plantations";
const defaultFileFolder = notesPath;
let fileFolder = defaultFileFolder;
let plantationsQuery = "";
switch (fileType) {
	case 'plantation':
		fileFolder = plantationsPath;
		plantationsQuery = '``````'
		break;
	case 'embryo':
		fileFolder = inboxPath
		break;
	}
const filePath = fileFolder + "/" + fullFileName
await tp.file.move(filePath)
%>---
aliases: <% fileName %>
dg-publish: true
created: <% dateNow %>
updated: <% dateNow %>
---
# <% fileName %>
---




###### META
Status:: #wiki/<% fileType %>
Plantations:: 
References:: 
```