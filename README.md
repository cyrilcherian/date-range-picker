JQuery Date Range Picker
=====================

Provides implementation to select date range. 


**INFO:** (Click) to select date range.

**INFO:** (CTRL + Click) to select/unselect date.

**INFO:** For Mac Users (Command + Click) to select/unselect date.

*Requires JQuery and JQuery-UI*

## Using the plugin

* For Date Range Picker on div: [Demo](http://cyrilcherian.github.io/date-range-picker/demo/datepickerdiv.html)
* For Date Range Picker on input: [Demo](http://cyrilcherian.github.io/date-range-picker/demo/datepickerinput.html)
* For Date Range Picker with selected date range and excluded dates: [Demo](http://cyrilcherian.github.io/date-range-picker/demo/datepickerexcluded.html)
* For Date Range Picker with disbled selection: [Demo](http://cyrilcherian.github.io/date-range-picker/demo/datepickerselectionoff.html)


## Usage

# How to set data.

Include all javascripts and CSS

- **Include the CSS**
- _The jquery UI CSS_ jquery-ui.css
- _The date range picker CSS_ date-range-picker.css
- **Include the javascripts**
- jquery.min.js
- jquery-ui.js
- date-range-picker.js

Example:
```html
    <link rel="stylesheet" href="../css/jquery-ui.css">
    <link rel="stylesheet" href="../css/date-range-picker.css">
    <script type="text/javascript" src="../lib/jquery.min.js"></script>
    <script type="text/javascript" src="../lib/jquery-ui.js"></script>
    <script type="text/javascript" src="../js/date-range-picker.js"></script>
```

Create your datepicker simply by:

```javascript
    var drp = $("#myDate").datepicker({});
```

Create your datepicker with disabled/excluded dates example:
```javascript
   //list of disabled dates these dates cannot be selected
    var disableddates = [new Date("3/12/2014"), new Date("3/14/2014")]
    //list of dates that needs to be selected
    var daterange = [new Date("3/1/2014"),new Date("3/2/2014"),new Date("3/3/2014")
    , new Date("3/20/2014")];
    //here myDate is the id of the div or input field to which we are making the date range picker.
    var drp = $("#myDate").datepicker({daterange:daterange, disableddates:disableddates});
```

# How to get selected date range.

```javascript
    //suppose drp stores the instance of the datepicker.
    //this will return an array of selected date instances.
    drp.getDateRange()
    
```
# How to disable selection.
You can disable full selection with disabled/excluded _this can be helpfull in non edit mode_ dates example:
```javascript
   //list of disabled dates these dates cannot be selected
    var disableddates = [new Date("3/12/2014"), new Date("3/14/2014")]
    //list of dates that needs to be selected
    var daterange = [new Date("3/1/2014"),new Date("3/2/2014"),new Date("3/3/2014")
    , new Date("3/20/2014")];
    //here myDate is the id of the div or input field to which we are making the date range picker.
    //Selection is disabled by passing enableSelection: false
    var drp = $("#myDate").datepicker({enableSelection: false, daterange:daterange, disableddates:disableddates});
```



