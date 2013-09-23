MonthPicker
===========

It's a modification of jquery ui datepicker to display a monthpicker. All configurable elements were kept. It's posible to use jquery ui theme.
So you can see documentation here [http://api.jqueryui.com/datepicker/](http://api.jqueryui.com/datepicker/).
![example][doc/example.png]

Modification
============

Some feature is change from the databpicker.

changeMonth
-----------
Removed

firstDay
--------
Removed

numberOfMonths
--------------
Renamed in numberOfYears

selectOtherMonths
-----------------
Removed

showOtherMonthsType
-------------------
Removed

showWeek
--------
Removed

stepMonths
----------
Removed

weekHeader
----------
Removed

Examples
========

```html
<!doctype html>
<html lang="us">
<head>
	<meta charset="utf-8">
	<title>Month picker Example Page</title>
	<link href="css/ui-lightness/jquery-ui-1.10.3.custom.css" rel="stylesheet">
	<link rel="stylesheet" href="http://code.jquery.com/ui/1.10.3/themes/smoothness/jquery-ui.css">
	<script src="http://code.jquery.com/jquery-1.9.1.js"></script>
	<script src="http://code.jquery.com/ui/1.10.3/jquery-ui.js"></script>
	<script src="jquery-tcm-monthpicker.js"></script>
	<script>
	$(function() {
		$( "#datepickermonthi" ).monthpicker();
	});
	</script>
<body>
<div id="datepickermonth"><div/>
</body>
</html>
```

























altFieldType: Selector or jQuery or Element
Default: ""
An input element that is to be updated with the selected date from the datepicker. Use the altFormat option to change the format of the date within this field. Leave as blank for no alternate field.
Code examples:

Initialize the datepicker with the altField option specified:
1
	

$( ".selector" ).datepicker({ altField: "#actualDate" });

Get or set the altField option, after initialization:
1
2
3
4
5
6
	

// getter
var altField = $( ".selector" ).datepicker( "option", "altField" );
// setter
$( ".selector" ).datepicker( "option", "altField", "#actualDate" );

altFormatType: String
Default: ""
The dateFormat to be used for the altField option. This allows one date format to be shown to the user for selection purposes, while a different format is actually sent behind the scenes. For a full list of the possible formats see the formatDate function
Code examples:

Initialize the datepicker with the altFormat option specified:
1
	

$( ".selector" ).datepicker({ altFormat: "yy-mm-dd" });

Get or set the altFormat option, after initialization:
1
2
3
4
5
6
	

// getter
var altFormat = $( ".selector" ).datepicker( "option", "altFormat" );
// setter
$( ".selector" ).datepicker( "option", "altFormat", "yy-mm-dd" );

appendTextType: String
Default: ""
The text to display after each date field, e.g., to show the required format.
Code examples:

Initialize the datepicker with the appendText option specified:
1
	

$( ".selector" ).datepicker({ appendText: "(yyyy-mm-dd)" });

Get or set the appendText option, after initialization:
1
2
3
4
5
6
	

// getter
var appendText = $( ".selector" ).datepicker( "option", "appendText" );
// setter
$( ".selector" ).datepicker( "option", "appendText", "(yyyy-mm-dd)" );

autoSizeType: Boolean
Default: false
Set to true to automatically resize the input field to accommodate dates in the current dateFormat.
Code examples:

Initialize the datepicker with the autoSize option specified:
1
	

$( ".selector" ).datepicker({ autoSize: true });

Get or set the autoSize option, after initialization:
1
2
3
4
5
6
	

// getter
var autoSize = $( ".selector" ).datepicker( "option", "autoSize" );
// setter
$( ".selector" ).datepicker( "option", "autoSize", true );

beforeShowType: Function( Element input, Object inst )
Default: null
A function that takes an input field and current datepicker instance and returns an options object to update the datepicker with. It is called just before the datepicker is displayed.
beforeShowDayType: Function( Date date )
Default: null
A function that takes a date as a parameter and must return an array with:

    [0]: true/false indicating whether or not this date is selectable
    [1]: a CSS class name to add to the date's cell or "" for the default presentation
    [2]: an optional popup tooltip for this date

The function is called for each day in the datepicker before it is displayed.
buttonImageType: String
Default: ""
A URL of an image to use to display the datepicker when the showOn option is set to "button" or "both". If set, the buttonText option becomes the alt value and is not directly displayed.
Code examples:

Initialize the datepicker with the buttonImage option specified:
1
	

$( ".selector" ).datepicker({ buttonImage: "/images/datepicker.gif" });

Get or set the buttonImage option, after initialization:
1
2
3
4
5
6
	

// getter
var buttonImage = $( ".selector" ).datepicker( "option", "buttonImage" );
// setter
$( ".selector" ).datepicker( "option", "buttonImage", "/images/datepicker.gif" );

buttonImageOnlyType: Boolean
Default: false
Whether the button image should be rendered by itself instead of inside a button element. This option is only relevant if the buttonImage option has also been set.
Code examples:

Initialize the datepicker with the buttonImageOnly option specified:
1
	

$( ".selector" ).datepicker({ buttonImageOnly: true });

Get or set the buttonImageOnly option, after initialization:
1
2
3
4
5
6
	

// getter
var buttonImageOnly = $( ".selector" ).datepicker( "option", "buttonImageOnly" );
// setter
$( ".selector" ).datepicker( "option", "buttonImageOnly", true );

buttonTextType: String
Default: "..."
The text to display on the trigger button. Use in conjunction with the showOn option set to "button" or "both".
Code examples:

Initialize the datepicker with the buttonText option specified:
1
	

$( ".selector" ).datepicker({ buttonText: "Choose" });

Get or set the buttonText option, after initialization:
1
2
3
4
5
6
	

// getter
var buttonText = $( ".selector" ).datepicker( "option", "buttonText" );
// setter
$( ".selector" ).datepicker( "option", "buttonText", "Choose" );

calculateWeekType: Function()
Default: jQuery.datepicker.iso8601Week
A function to calculate the week of the year for a given date. The default implementation uses the ISO 8601 definition: weeks start on a Monday; the first week of the year contains the first Thursday of the year.
Code examples:

Initialize the datepicker with the calculateWeek option specified:
1
	

$( ".selector" ).datepicker({ calculateWeek: myWeekCalc });

Get or set the calculateWeek option, after initialization:
1
2
3
4
5
6
	

// getter
var calculateWeek = $( ".selector" ).datepicker( "option", "calculateWeek" );
// setter
$( ".selector" ).datepicker( "option", "calculateWeek", myWeekCalc );

changeMonthType: Boolean
Default: false
Whether the month should be rendered as a dropdown instead of text.
Code examples:

Initialize the datepicker with the changeMonth option specified:
1
	

$( ".selector" ).datepicker({ changeMonth: true });

Get or set the changeMonth option, after initialization:
1
2
3
4
5
6
	

// getter
var changeMonth = $( ".selector" ).datepicker( "option", "changeMonth" );
// setter
$( ".selector" ).datepicker( "option", "changeMonth", true );

changeYearType: Boolean
Default: false
Whether the year should be rendered as a dropdown instead of text. Use the yearRange option to control which years are made available for selection.
Code examples:

Initialize the datepicker with the changeYear option specified:
1
	

$( ".selector" ).datepicker({ changeYear: true });

Get or set the changeYear option, after initialization:
1
2
3
4
5
6
	

// getter
var changeYear = $( ".selector" ).datepicker( "option", "changeYear" );
// setter
$( ".selector" ).datepicker( "option", "changeYear", true );

closeTextType: String
Default: "Done"
The text to display for the close link. Use the showButtonPanel option to display this button.
Code examples:

Initialize the datepicker with the closeText option specified:
1
	

$( ".selector" ).datepicker({ closeText: "Close" });

Get or set the closeText option, after initialization:
1
2
3
4
5
6
	

// getter
var closeText = $( ".selector" ).datepicker( "option", "closeText" );
// setter
$( ".selector" ).datepicker( "option", "closeText", "Close" );

constrainInputType: Boolean
Default: true
When true, entry in the input field is constrained to those characters allowed by the current dateFormat option.
Code examples:

Initialize the datepicker with the constrainInput option specified:
1
	

$( ".selector" ).datepicker({ constrainInput: false });

Get or set the constrainInput option, after initialization:
1
2
3
4
5
6
	

// getter
var constrainInput = $( ".selector" ).datepicker( "option", "constrainInput" );
// setter
$( ".selector" ).datepicker( "option", "constrainInput", false );

currentTextType: String
Default: "Today"
The text to display for the current day link. Use the showButtonPanel option to display this button.
Code examples:

Initialize the datepicker with the currentText option specified:
1
	

$( ".selector" ).datepicker({ currentText: "Now" });

Get or set the currentText option, after initialization:
1
2
3
4
5
6
	

// getter
var currentText = $( ".selector" ).datepicker( "option", "currentText" );
// setter
$( ".selector" ).datepicker( "option", "currentText", "Now" );

dateFormatType: String
Default: "mm/dd/yy"
The format for parsed and displayed dates. For a full list of the possible formats see the formatDate function.
Code examples:

Initialize the datepicker with the dateFormat option specified:
1
	

$( ".selector" ).datepicker({ dateFormat: "yy-mm-dd" });

Get or set the dateFormat option, after initialization:
1
2
3
4
5
6
	

// getter
var dateFormat = $( ".selector" ).datepicker( "option", "dateFormat" );
// setter
$( ".selector" ).datepicker( "option", "dateFormat", "yy-mm-dd" );

dayNamesType: Array
Default: [ "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday" ]
The list of long day names, starting from Sunday, for use as requested via the dateFormat option.
Code examples:

Initialize the datepicker with the dayNames option specified:
1
	

$( ".selector" ).datepicker({ dayNames: [ "Dimanche", "Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi" ] });

Get or set the dayNames option, after initialization:
1
2
3
4
5
6
	

// getter
var dayNames = $( ".selector" ).datepicker( "option", "dayNames" );
// setter
$( ".selector" ).datepicker( "option", "dayNames", [ "Dimanche", "Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi" ] );

dayNamesMinType: Array
Default: [ "Su", "Mo", "Tu", "We", "Th", "Fr", "Sa" ]
The list of minimised day names, starting from Sunday, for use as column headers within the datepicker.
Code examples:

Initialize the datepicker with the dayNamesMin option specified:
1
	

$( ".selector" ).datepicker({ dayNamesMin: [ "Di", "Lu", "Ma", "Me", "Je", "Ve", "Sa" ] });

Get or set the dayNamesMin option, after initialization:
1
2
3
4
5
6
	

// getter
var dayNamesMin = $( ".selector" ).datepicker( "option", "dayNamesMin" );
// setter
$( ".selector" ).datepicker( "option", "dayNamesMin", [ "Di", "Lu", "Ma", "Me", "Je", "Ve", "Sa" ] );

dayNamesShortType: Array
Default: [ "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" ]
The list of abbreviated day names, starting from Sunday, for use as requested via the dateFormat option.
Code examples:

Initialize the datepicker with the dayNamesShort option specified:
1
	

$( ".selector" ).datepicker({ dayNamesShort: [ "Dim", "Lun", "Mar", "Mer", "Jeu", "Ven", "Sam" ] });

Get or set the dayNamesShort option, after initialization:
1
2
3
4
5
6
	

// getter
var dayNamesShort = $( ".selector" ).datepicker( "option", "dayNamesShort" );
// setter
$( ".selector" ).datepicker( "option", "dayNamesShort", [ "Dim", "Lun", "Mar", "Mer", "Jeu", "Ven", "Sam" ] );

defaultDateType: Date or Number or String
Default: null
Set the date to highlight on first opening if the field is blank. Specify either an actual date via a Date object or as a string in the current dateFormat, or a number of days from today (e.g. +7) or a string of values and periods ('y' for years, 'm' for months, 'w' for weeks, 'd' for days, e.g. '+1m +7d'), or null for today.
Multiple types supported:

    Date: A date object containing the default date.
    Number: A number of days from today. For example 2 represents two days from today and -1 represents yesterday.
    String: A string in the format defined by the dateFormat option, or a relative date. Relative dates must contain value and period pairs; valid periods are "y" for years, "m" for months, "w" for weeks, and "d" for days. For example, "+1m +7d" represents one month and seven days from today.

Code examples:

Initialize the datepicker with the defaultDate option specified:
1
	

$( ".selector" ).datepicker({ defaultDate: +7 });

Get or set the defaultDate option, after initialization:
1
2
3
4
5
6
	

// getter
var defaultDate = $( ".selector" ).datepicker( "option", "defaultDate" );
// setter
$( ".selector" ).datepicker( "option", "defaultDate", +7 );

durationType: or String
Default: "normal"
Control the speed at which the datepicker appears, it may be a time in milliseconds or a string representing one of the three predefined speeds ("slow", "normal", "fast").
Code examples:

Initialize the datepicker with the duration option specified:
1
	

$( ".selector" ).datepicker({ duration: "slow" });

Get or set the duration option, after initialization:
1
2
3
4
5
6
	

// getter
var duration = $( ".selector" ).datepicker( "option", "duration" );
// setter
$( ".selector" ).datepicker( "option", "duration", "slow" );

firstDayType: Integer
Default: 0
Set the first day of the week: Sunday is 0, Monday is 1, etc.
Code examples:

Initialize the datepicker with the firstDay option specified:
1
	

$( ".selector" ).datepicker({ firstDay: 1 });

Get or set the firstDay option, after initialization:
1
2
3
4
5
6
	

// getter
var firstDay = $( ".selector" ).datepicker( "option", "firstDay" );
// setter
$( ".selector" ).datepicker( "option", "firstDay", 1 );

gotoCurrentType: Boolean
Default: false
When true, the current day link moves to the currently selected date instead of today.
Code examples:

Initialize the datepicker with the gotoCurrent option specified:
1
	

$( ".selector" ).datepicker({ gotoCurrent: true });

Get or set the gotoCurrent option, after initialization:
1
2
3
4
5
6
	

// getter
var gotoCurrent = $( ".selector" ).datepicker( "option", "gotoCurrent" );
// setter
$( ".selector" ).datepicker( "option", "gotoCurrent", true );

hideIfNoPrevNextType: Boolean
Default: false
Normally the previous and next links are disabled when not applicable (see the minDate and maxDate options). You can hide them altogether by setting this attribute to true.
Code examples:

Initialize the datepicker with the hideIfNoPrevNext option specified:
1
	

$( ".selector" ).datepicker({ hideIfNoPrevNext: true });

Get or set the hideIfNoPrevNext option, after initialization:
1
2
3
4
5
6
	

// getter
var hideIfNoPrevNext = $( ".selector" ).datepicker( "option", "hideIfNoPrevNext" );
// setter
$( ".selector" ).datepicker( "option", "hideIfNoPrevNext", true );

isRTLType: Boolean
Default: false
Whether the current language is drawn from right to left.
Code examples:

Initialize the datepicker with the isRTL option specified:
1
	

$( ".selector" ).datepicker({ isRTL: true });

Get or set the isRTL option, after initialization:
1
2
3
4
5
6
	

// getter
var isRTL = $( ".selector" ).datepicker( "option", "isRTL" );
// setter
$( ".selector" ).datepicker( "option", "isRTL", true );

maxDateType: Date or Number or String
Default: null
The maximum selectable date. When set to null, there is no maximum.
Multiple types supported:

    Date: A date object containing the maximum date.
    Number: A number of days from today. For example 2 represents two days from today and -1 represents yesterday.
    String: A string in the format defined by the dateFormat option, or a relative date. Relative dates must contain value and period pairs; valid periods are "y" for years, "m" for months, "w" for weeks, and "d" for days. For example, "+1m +7d" represents one month and seven days from today.

Code examples:

Initialize the datepicker with the maxDate option specified:
1
	

$( ".selector" ).datepicker({ maxDate: "+1m +1w" });

Get or set the maxDate option, after initialization:
1
2
3
4
5
6
	

// getter
var maxDate = $( ".selector" ).datepicker( "option", "maxDate" );
// setter
$( ".selector" ).datepicker( "option", "maxDate", "+1m +1w" );

minDateType: Date or Number or String
Default: null
The minimum selectable date. When set to null, there is no minimum.
Multiple types supported:

    Date: A date object containing the minimum date.
    Number: A number of days from today. For example 2 represents two days from today and -1 represents yesterday.
    String: A string in the format defined by the dateFormat option, or a relative date. Relative dates must contain value and period pairs; valid periods are "y" for years, "m" for months, "w" for weeks, and "d" for days. For example, "+1m +7d" represents one month and seven days from today.

Code examples:

Initialize the datepicker with the minDate option specified:
1
	

$( ".selector" ).datepicker({ minDate: new Date(2007, 1 - 1, 1) });

Get or set the minDate option, after initialization:
1
2
3
4
5
6
	

// getter
var minDate = $( ".selector" ).datepicker( "option", "minDate" );
// setter
$( ".selector" ).datepicker( "option", "minDate", new Date(2007, 1 - 1, 1) );

monthNamesType: Array
Default: [ "January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December" ]
The list of full month names, for use as requested via the dateFormat option.
Code examples:

Initialize the datepicker with the monthNames option specified:
1
	

$( ".selector" ).datepicker({ monthNames: [ "Januar", "Februar", "Marts", "April", "Maj", "Juni", "Juli", "August", "September", "Oktober", "November", "December" ] });

Get or set the monthNames option, after initialization:
1
2
3
4
5
6
	

// getter
var monthNames = $( ".selector" ).datepicker( "option", "monthNames" );
// setter
$( ".selector" ).datepicker( "option", "monthNames", [ "Januar", "Februar", "Marts", "April", "Maj", "Juni", "Juli", "August", "September", "Oktober", "November", "December" ] );

monthNamesShortType: Array
Default: [ "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec" ]
The list of abbreviated month names, as used in the month header on each datepicker and as requested via the dateFormat option.
Code examples:

Initialize the datepicker with the monthNamesShort option specified:
1
	

$( ".selector" ).datepicker({ monthNamesShort: [ "Jan", "Feb", "Mar", "Apr", "Maj", "Jun", "Jul", "Aug", "Sep", "Okt", "Nov", "Dec" ] });

Get or set the monthNamesShort option, after initialization:
1
2
3
4
5
6
	

// getter
var monthNamesShort = $( ".selector" ).datepicker( "option", "monthNamesShort" );
// setter
$( ".selector" ).datepicker( "option", "monthNamesShort", [ "Jan", "Feb", "Mar", "Apr", "Maj", "Jun", "Jul", "Aug", "Sep", "Okt", "Nov", "Dec" ] );

navigationAsDateFormatType: Boolean
Default: false
Whether the prevText and nextText options should be parsed as dates by the formatDate function, allowing them to display the target month names for example.
Code examples:

Initialize the datepicker with the navigationAsDateFormat option specified:
1
	

$( ".selector" ).datepicker({ navigationAsDateFormat: true });

Get or set the navigationAsDateFormat option, after initialization:
1
2
3
4
5
6
	

// getter
var navigationAsDateFormat = $( ".selector" ).datepicker( "option", "navigationAsDateFormat" );
// setter
$( ".selector" ).datepicker( "option", "navigationAsDateFormat", true );

nextTextType: String
Default: "Next"
The text to display for the next month link. With the standard ThemeRoller styling, this value is replaced by an icon.
Code examples:

Initialize the datepicker with the nextText option specified:
1
	

$( ".selector" ).datepicker({ nextText: "Later" });

Get or set the nextText option, after initialization:
1
2
3
4
5
6
	

// getter
var nextText = $( ".selector" ).datepicker( "option", "nextText" );
// setter
$( ".selector" ).datepicker( "option", "nextText", "Later" );

numberOfMonthsType: Number or Array
Default: 1
The number of months to show at once.
Multiple types supported:

    Number: The number of months to display in a single row.
    Array: An array defining the number of rows and columns to display.

Code examples:

Initialize the datepicker with the numberOfMonths option specified:
1
	

$( ".selector" ).datepicker({ numberOfMonths: [ 2, 3 ] });

Get or set the numberOfMonths option, after initialization:
1
2
3
4
5
6
	

// getter
var numberOfMonths = $( ".selector" ).datepicker( "option", "numberOfMonths" );
// setter
$( ".selector" ).datepicker( "option", "numberOfMonths", [ 2, 3 ] );

onChangeMonthYearType: Function( Integer year, Integer month, Object inst )
Default: null
Called when the datepicker moves to a new month and/or year. The function receives the selected year, month (1-12), and the datepicker instance as parameters. this refers to the associated input field.
onCloseType: Function( String dateText, Object inst )
Default: null
Called when the datepicker is closed, whether or not a date is selected. The function receives the selected date as text ("" if none) and the datepicker instance as parameters. this refers to the associated input field.
onSelectType: Function( String dateText, Object inst )
Default: null
Called when the datepicker is selected. The function receives the selected date as text and the datepicker instance as parameters. this refers to the associated input field.
prevTextType: String
Default: "Prev"
The text to display for the previous month link. With the standard ThemeRoller styling, this value is replaced by an icon.
Code examples:

Initialize the datepicker with the prevText option specified:
1
	

$( ".selector" ).datepicker({ prevText: "Earlier" });

Get or set the prevText option, after initialization:
1
2
3
4
5
6
	

// getter
var prevText = $( ".selector" ).datepicker( "option", "prevText" );
// setter
$( ".selector" ).datepicker( "option", "prevText", "Earlier" );

selectOtherMonthsType: Boolean
Default: false
Whether days in other months shown before or after the current month are selectable. This only applies if the showOtherMonths option is set to true.
Code examples:

Initialize the datepicker with the selectOtherMonths option specified:
1
	

$( ".selector" ).datepicker({ selectOtherMonths: true });

Get or set the selectOtherMonths option, after initialization:
1
2
3
4
5
6
	

// getter
var selectOtherMonths = $( ".selector" ).datepicker( "option", "selectOtherMonths" );
// setter
$( ".selector" ).datepicker( "option", "selectOtherMonths", true );

shortYearCutoffType: Number or String
Default: "+10"
The cutoff year for determining the century for a date (used in conjunction with dateFormat 'y'). Any dates entered with a year value less than or equal to the cutoff year are considered to be in the current century, while those greater than it are deemed to be in the previous century.
Multiple types supported:

    Number: A value between 0 and 99 indicating the cutoff year.
    String: A relative number of years from the current year, e.g., "+3" or "-5".

Code examples:

Initialize the datepicker with the shortYearCutoff option specified:
1
	

$( ".selector" ).datepicker({ shortYearCutoff: 50 });

Get or set the shortYearCutoff option, after initialization:
1
2
3
4
5
6
	

// getter
var shortYearCutoff = $( ".selector" ).datepicker( "option", "shortYearCutoff" );
// setter
$( ".selector" ).datepicker( "option", "shortYearCutoff", 50 );

showAnimType: String
Default: "show"
The name of the animation used to show and hide the datepicker. Use "show" (the default), "slideDown", "fadeIn", any of the jQuery UI effects. Set to an empty string to disable animation.
Code examples:

Initialize the datepicker with the showAnim option specified:
1
	

$( ".selector" ).datepicker({ showAnim: "fold" });

Get or set the showAnim option, after initialization:
1
2
3
4
5
6
	

// getter
var showAnim = $( ".selector" ).datepicker( "option", "showAnim" );
// setter
$( ".selector" ).datepicker( "option", "showAnim", "fold" );

showButtonPanelType: Boolean
Default: false
Whether to display a button pane underneath the calendar. The button pane contains two buttons, a Today button that links to the current day, and a Done button that closes the datepicker. The buttons' text can be customized using the currentText and closeText options respectively.
Code examples:

Initialize the datepicker with the showButtonPanel option specified:
1
	

$( ".selector" ).datepicker({ showButtonPanel: true });

Get or set the showButtonPanel option, after initialization:
1
2
3
4
5
6
	

// getter
var showButtonPanel = $( ".selector" ).datepicker( "option", "showButtonPanel" );
// setter
$( ".selector" ).datepicker( "option", "showButtonPanel", true );

showCurrentAtPosType: Number
Default: 0
When displaying multiple months via the numberOfMonths option, the showCurrentAtPos option defines which position to display the current month in.
Code examples:

Initialize the datepicker with the showCurrentAtPos option specified:
1
	

$( ".selector" ).datepicker({ showCurrentAtPos: 3 });

Get or set the showCurrentAtPos option, after initialization:
1
2
3
4
5
6
	

// getter
var showCurrentAtPos = $( ".selector" ).datepicker( "option", "showCurrentAtPos" );
// setter
$( ".selector" ).datepicker( "option", "showCurrentAtPos", 3 );

showMonthAfterYearType: Boolean
Default: false
Whether to show the month after the year in the header.
Code examples:

Initialize the datepicker with the showMonthAfterYear option specified:
1
	

$( ".selector" ).datepicker({ showMonthAfterYear: true });

Get or set the showMonthAfterYear option, after initialization:
1
2
3
4
5
6
	

// getter
var showMonthAfterYear = $( ".selector" ).datepicker( "option", "showMonthAfterYear" );
// setter
$( ".selector" ).datepicker( "option", "showMonthAfterYear", true );

showOnType: String
Default: "focus"
When the datepicker should appear. The datepicker can appear when the field receives focus ("focus"), when a button is clicked ("button"), or when either event occurs ("both").
Code examples:

Initialize the datepicker with the showOn option specified:
1
	

$( ".selector" ).datepicker({ showOn: "both" });

Get or set the showOn option, after initialization:
1
2
3
4
5
6
	

// getter
var showOn = $( ".selector" ).datepicker( "option", "showOn" );
// setter
$( ".selector" ).datepicker( "option", "showOn", "both" );

showOptionsType: Object
Default: {}
If using one of the jQuery UI effects for the showAnim option, you can provide additional settings for that animation via this option.
Code examples:

Initialize the datepicker with the showOptions option specified:
1
	

$( ".selector" ).datepicker({ showOptions: { direction: "up" } });

Get or set the showOptions option, after initialization:
1
2
3
4
5
6
	

// getter
var showOptions = $( ".selector" ).datepicker( "option", "showOptions" );
// setter
$( ".selector" ).datepicker( "option", "showOptions", { direction: "up" } );

showOtherMonthsType: Boolean
Default: false
Whether to display dates in other months (non-selectable) at the start or end of the current month. To make these days selectable use the selectOtherMonths option.
Code examples:

Initialize the datepicker with the showOtherMonths option specified:
1
	

$( ".selector" ).datepicker({ showOtherMonths: true });

Get or set the showOtherMonths option, after initialization:
1
2
3
4
5
6
	

// getter
var showOtherMonths = $( ".selector" ).datepicker( "option", "showOtherMonths" );
// setter
$( ".selector" ).datepicker( "option", "showOtherMonths", true );

showWeekType: Boolean
Default: false
When true, a column is added to show the week of the year. The calculateWeek option determines how the week of the year is calculated. You may also want to change the firstDay option.
Code examples:

Initialize the datepicker with the showWeek option specified:
1
	

$( ".selector" ).datepicker({ showWeek: true });

Get or set the showWeek option, after initialization:
1
2
3
4
5
6
	

// getter
var showWeek = $( ".selector" ).datepicker( "option", "showWeek" );
// setter
$( ".selector" ).datepicker( "option", "showWeek", true );

stepMonthsType: Number
Default: 1
Set how many months to move when clicking the previous/next links.
Code examples:

Initialize the datepicker with the stepMonths option specified:
1
	

$( ".selector" ).datepicker({ stepMonths: 3 });

Get or set the stepMonths option, after initialization:
1
2
3
4
5
6
	

// getter
var stepMonths = $( ".selector" ).datepicker( "option", "stepMonths" );
// setter
$( ".selector" ).datepicker( "option", "stepMonths", 3 );

weekHeaderType: String
Default: "Wk"
The text to display for the week of the year column heading. Use the showWeek option to display this column.
Code examples:

Initialize the datepicker with the weekHeader option specified:
1
	

$( ".selector" ).datepicker({ weekHeader: "W" });

Get or set the weekHeader option, after initialization:
1
2
3
4
5
6
	

// getter
var weekHeader = $( ".selector" ).datepicker( "option", "weekHeader" );
// setter
$( ".selector" ).datepicker( "option", "weekHeader", "W" );

yearRangeType: String
Default: "c-10:c+10"
The range of years displayed in the year drop-down: either relative to today's year ("-nn:+nn"), relative to the currently selected year ("c-nn:c+nn"), absolute ("nnnn:nnnn"), or combinations of these formats ("nnnn:-nn"). Note that this option only affects what appears in the drop-down, to restrict which dates may be selected use the minDate and/or maxDate options.
Code examples:

Initialize the datepicker with the yearRange option specified:
1
	

$( ".selector" ).datepicker({ yearRange: "2002:2012" });

Get or set the yearRange option, after initialization:
1
2
3
4
5
6
	

// getter
var yearRange = $( ".selector" ).datepicker( "option", "yearRange" );
// setter
$( ".selector" ).datepicker( "option", "yearRange", "2002:2012" );

yearSuffixType: String
Default: ""
Additional text to display after the year in the month headers.
Code examples:

Initialize the datepicker with the yearSuffix option specified:
1
	

$( ".selector" ).datepicker({ yearSuffix: "CE" });

Get or set the yearSuffix option, after initialization:
1
2
3
4
5
6
	

// getter
var yearSuffix = $( ".selector" ).datepicker( "option", "yearSuffix" );
// setter
$( ".selector" ).datepicker( "option", "yearSuffix", "CE" );

Methods
destroy()
Removes the datepicker functionality completely. This will return the element back to its pre-init state.

    This method does not accept any arguments.

Code examples:

Invoke the destroy method:
1
	

$( ".selector" ).datepicker( "destroy" );

dialog( date [, onSelect ] [, settings ] [, pos ] )
Opens the datepicker in a dialog box.

    date
    Type: String or Date
    The initial date.
    onSelect
    Type: Function()
    A callback function when a date is selected. The function receives the date text and date picker instance as parameters.
    settings
    Type: Options
    The new settings for the date picker.
    pos
    Type: Number[2] or MouseEvent
    The position of the top/left of the dialog as [x, y] or a MouseEvent that contains the coordinates. If not specified the dialog is centered on the screen.

Code examples:

Invoke the dialog method:
1
	

$( ".selector" ).datepicker( "dialog", "10/12/2012" );

getDate()Returns: Date
Returns the current date for the datepicker or null if no date has been selected.

    This method does not accept any arguments.

Code examples:

Invoke the getDate method:
1
	

var currentDate = $( ".selector" ).datepicker( "getDate" );

hide()
Close a previously opened date picker.

    This method does not accept any arguments.

Code examples:

Invoke the hide method:
1
	

$( ".selector" ).datepicker( "hide" );

isDisabled()Returns: Boolean
Determine whether a date picker has been disabled.

    This method does not accept any arguments.

Code examples:

Invoke the isDisabled method:
1
	

var isDisabled = $( ".selector" ).datepicker( "isDisabled" );

option( optionName )Returns: Object
Gets the value currently associated with the specified optionName.

    optionName
    Type: String
    The name of the option to get.

Code examples:

Invoke the method:
1
	

var isDisabled = $( ".selector" ).datepicker( "option", "disabled" );

option()Returns: PlainObject
Gets an object containing key/value pairs representing the current datepicker options hash.

    This method does not accept any arguments.

Code examples:

Invoke the method:
1
	

var options = $( ".selector" ).datepicker( "option" );

option( optionName, value )
Sets the value of the datepicker option associated with the specified optionName.

    optionName
    Type: String
    The name of the option to set.
    value
    Type: Object
    A value to set for the option.

Code examples:

Invoke the method:
1
	

$( ".selector" ).datepicker( "option", "disabled", true );

option( options )
Sets one or more options for the datepicker.

    options
    Type: Object
    A map of option-value pairs to set.

Code examples:

Invoke the method:
1
	

$( ".selector" ).datepicker( "option", { disabled: true } );

refresh()
Redraw the date picker, after having made some external modifications.

    This method does not accept any arguments.

Code examples:

Invoke the refresh method:
1
	

$( ".selector" ).datepicker( "refresh" );

setDate( date )
Sets the date for the datepicker. The new date may be a Date object or a string in the current date format (e.g., "01/26/2009"), a number of days from today (e.g., +7) or a string of values and periods ("y" for years, "m" for months, "w" for weeks, "d" for days, e.g., "+1m +7d"), or null to clear the selected date.

    date
    Type: String or Date
    The new date.

Code examples:

Invoke the setDate method:
1
	

$( ".selector" ).datepicker( "setDate", "10/12/2012" );

show()
Open the date picker. If the datepicker is attached to an input, the input must be visible for the datepicker to be shown.

    This method does not accept any arguments.

Code examples:

Invoke the show method:
1
	

$( ".selector" ).datepicker( "show" );

widget()Returns: jQuery
Returns a jQuery object containing the datepicker.

    This method does not accept any arguments.

Code examples:

Invoke the widget method:
1
	

var widget = $( ".selector" ).datepicker( "widget" );
