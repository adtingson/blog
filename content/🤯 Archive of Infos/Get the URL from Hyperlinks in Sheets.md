---
title: Get the URL from Hyperlinks in Google Sheets 🤓
draft: false
tags:
  - google-sheets
  - for-work
  - sheets-formula
  - get-URL
  - 🌱seedling
date: 2024-08-15
---
## Code for AppScripts

```
function GETLINK(input){
	var sheet = SpreadsheetApp.getActiveSheet();
	var range = sheet.getRange(input);
	var value = range.getRichTextValue();
	var url = value.getLinkUrl();
	return url;
}
```

## Formula for Sheets

```
=GETLINK(CELL("Address", A2))
```
