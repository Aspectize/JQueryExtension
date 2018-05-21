# JQueryExtension
Aspectize Extension to misc JQuery plugin: JQueryMask, JQueryColorPicker, JQueryDatePicker.

JQueryAutoComplete from this extension is obsolete. Use specific Extension JQueryAutoComplete instead.

## 1 - Download

Download extension package from aspectize.com:
- in the portal, goto extension section
- browse extension, and find JQueryExtension
- download package and unzip it into your local WebHost Applications directory; you should have a JQueryExtension directory next to your app directory.

## 2 - Configuration

Add JQueryExtension as Shared Application in your application configuration file.
In your Visual Studio Project, find the file Application.js in the Configuration folder.

Add JQueryExtension in the Directories list :
```javascript
app.Directories = "... , JQueryExtension";
```

## 3 - Include js and css

In your application.htm.ashx file, depending on witch plugin you will use, add the following files included: these are standard files from jquery and jquery-ui plugin.
```javascript
<!-- JQuery Color Picker -->
<link href="~JQueryExtension/jquery-miniColors/jquery.miniColors.css" media="all" rel="stylesheet" type="text/css"/> 
<script language="javascript" src="~JQueryExtension/jquery-miniColors/jquery.miniColors.min.js" type="text/javascript"></script> 

<!-- JQuery Mask -->
<script type="text/javascript" src="~JQueryExtension/jQuery-Mask-Plugin-master/jquery.mask.min.js"></script>

```

## 4 - Usage

### 1 JQuery DatePicker

a/ Html

Insert the following html into your control:
```html
<input name="JQueryDatePickerSample" aas-type="JQueryExtension.JQueryDatePicker" readonly="readonly" type="text" />
```

b/ Binding

The following properties are bindable (references of properties are available here: http://api.jqueryui.com/datepicker):
- Value: date value.
- MinDate: minDate property. Default is null.
- MaxDate: maxDate property. Default is null
- DefaultDate: default is new Date().
- Mask: 
- DisplayFormat: 
- FirstDay: Default is 0.
- ChangeMonth: Default is false.
- ChangeYear: Default is false.
- YearRange: Default is 'c-10:c+10'.
- ShowButton: Default is true
- ShowOn: 
- WithTime: Default is false.
- ShowTime: Default is true.
- OnlyTime: Default is false
- StepMinute: Default is 1
- TimeZone: Default is null.

### 2 JQuery ColorPicker

a/ Html

Insert the following html into your control:
```html
<input name="TxtBackGroundColor" aas-type="JQueryExtension.JQueryColorPicker" />
```

b/ Binding

The following properties are bindable:
- Value: value of color in format #RRGGBB.
- DefaultValue: ''.
- InLine: if true, colorPicker is displayed inline. Default is false
- Theme: Default is 'default'.

### 3 JQuery Mask

a/ Html

Insert the following html into your control:
```html
<input name="TxtNumeroSecu" type="text" aas-type="JQueryExtension.JQueryMask" class="form-control" />
```

b/ Binding

The following properties are bindable:
