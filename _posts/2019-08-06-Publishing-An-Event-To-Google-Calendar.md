---
layout: post
title: Publishing An Event To Google Calendar 
tags: google-calendar google-apps-script javascript calendar 
---

Open up the script editor from the google sheet. When you come to run the sheet for the first time, you will be asked to permit that action. 


Using a string constructed to create an *A1* style notation to get the value of a cell: 

```javascript
var dt = sheet.getRange(dateID+ActiveRow).getValue();
```

Get the active sheet and the current row and the last row in the selection (assuming that the user selected a cell and then stretched it). 

```javascript
  var sheet = SpreadsheetApp.getActiveSheet();
  var first = sheet.getActiveRange().getRow();
  var last = sheet.getActiveRange().getLastRow();
```

*It's not entirely clear how to grab the first line of the selection* 


Grab a calendar by name. 
```javascript
    var calendars = CalendarApp.getCalendarsByName(cal);
```

Create an all day [event](https://developers.google.com/apps-script/reference/calendar/calendar-event): 

```javascript
var event = calendar.createAllDayEvent(title, new Date(y, m, d));
```


### Last things first 

In order to add the functionality to sheet itself: 


```javascript
function onOpen(e) {
  var menu = SpreadsheetApp.getUi().createAddonMenu(); // Or DocumentApp or FormApp.
  menu.addItem('The text for the menu item', 'TheNameOfTheFunction');
  menu.addToUi();
}
```


