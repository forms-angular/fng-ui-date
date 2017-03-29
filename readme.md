# fng-ui-date

Plugin for forms-angular that adds jQuery UI date picker.

## Usage

    bower install fng-ui-date
    
Add the following lines to your index.html (or equivalent) file

    <link rel="stylesheet" href="/bower_components/jquery-ui/themes/smoothness/jquery-ui.css">
    <script src="bower_components/angular-ui-date/dist/date.js"></script>
    
Date fields in models will have the date picker added.
    
## Configuration

Configure as part of your Angular app configuration as follows:

```
    myApp.config(['uiDateConfig', function(uiDateConfig) {
      angular.extend(uiDateConfig, {
        dateFormat: 'dd/mm/yy',             // UK date format
        firstDay: 1                         // Monday week start
      });
    }]);
```    

For detailed options see the documentation at http://jqueryui.com/datepicker/

You can specify the timezone (useful to specify UTC for dates of birth and other 'floating' dates) using the schema form.add property:
```
  dateOfBirth: {type: Date, form: {add: ' ng-model-options="{timezone:\'UTC\'}"'}}  

```
(see the dateOfBirth property in [this](https://www.forms-angular.org/models/b_enhanced_schema.js) schema for an example)

