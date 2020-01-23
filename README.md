
# Bootstrap 4 Datatable w/ AngularJS and FontAwesome 5

This project demonstrates a template for full-fledged, DISPLAY only (not updatable) datatable, including Export functionality, a Print Button, and Column Visibility.

## Datatables are AWESOME!!!

They can be used for displaying information in a whole new - INTERACTIVE - way on the web.   It used front-end technology (javascript- or more specifically jquery), and can be customized to any number of visual configurations.    But getting started with datatables can be a little complicated.  If you are not all that familiar with the working of datatables, the website https://datatables.net/ is a good place to start, but there is a TON of information... and it's not always current.  Versioning and style differences change the classes that are used. Whether you're using Bootstrap or jQueryUI or just a basic datatable.  It can be complicated.  

_My goal is to create a reusuable datatable template, with all of the button and export functionality you might need in a business enviroment.  The code included builds a basic datatable, with javacript table definitions. The primary underlying premise is user experience, how table appears in browser, with an eye towards maximum usability._

## What is this project NOT??
- It is not a CLI based project.  You do not need a CLI or other client-side build tool to run this datatable.  You simply need a server  local host should work, or any other webserver.  
- It is not a tutorial for Angular-Datatables.   Angular has it's own datatables library and this is not that.  This uses standard datatable libraries and is simply using AngularJS for includes. 


## Getting Started

Simply copy the code to your server, index.html should run the page.  No build tools are required.

### Prerequisites

Internet access to the CSS include files. 

```
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/jqueryui/1.12.1/themes/base/jquery-ui.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.18/css/dataTables.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/autofill/2.3.2/css/autoFill.bootstrap4.min.css"/>
	
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/buttons/1.5.4/css/buttons.jqueryui.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/buttons/1.5.4/css/buttons.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/colreorder/1.5.0/css/colReorder.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/fixedcolumns/3.2.5/css/fixedColumns.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/fixedheader/3.1.4/css/fixedHeader.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/keytable/2.5.0/css/keyTable.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/responsive/2.2.2/css/responsive.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/rowgroup/1.1.0/css/rowGroup.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/rowreorder/1.2.4/css/rowReorder.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/scroller/1.5.0/css/scroller.bootstrap4.css"/>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/select/1.2.6/css/select.bootstrap4.css"/>
```

Internet access to the Javascript include files. 

```
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jszip/2.5.0/jszip.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/pdfmake/0.1.36/pdfmake.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/pdfmake/0.1.36/vfs_fonts.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/1.10.18/js/jquery.dataTables.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/1.10.18/js/dataTables.bootstrap4.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/autofill/2.3.2/js/dataTables.autoFill.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/autofill/2.3.2/js/autoFill.bootstrap4.js"></script>
<script type="text/javascript" src="dataTables.buttons.js"></script>  <!-- use custom instead of CDN-->
<!--<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.5.4/js/buttons.bootstrap4.js"></script>-->

<script type="text/javascript" src="buttons.jquery-ui.js"></script><!-- use custom instead of CDN-->
<!--<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.5.4/js/buttons.jqueryui.js"></script>-->
<script type="text/javascript" src="buttons.colVis.js"></script><!-- use custom instead of CDN-->
<!--<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.5.4/js/buttons.colVis.js"></script>-->
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.5.4/js/buttons.flash.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.5.4/js/buttons.html5.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/buttons/1.5.4/js/buttons.print.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/colreorder/1.5.0/js/dataTables.colReorder.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/fixedcolumns/3.2.5/js/dataTables.fixedColumns.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/fixedheader/3.1.4/js/dataTables.fixedHeader.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/keytable/2.5.0/js/dataTables.keyTable.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/responsive/2.2.2/js/dataTables.responsive.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/rowgroup/1.1.0/js/dataTables.rowGroup.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/rowreorder/1.2.4/js/dataTables.rowReorder.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/scroller/1.5.0/js/dataTables.scroller.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/select/1.2.6/js/dataTables.select.js"></script>
```

### Installing

No installation necessary.  It's all client side, simply run on localhost or webserver.



## Built With

### [Bootstrap 4x](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
After several years of heavily using Bootstrap 3x, this was my first opportunity to dive into the new (Twitter) Bootstrap 4.  There are many differences, between Bootstrap 3 and 4.  The main upgrade is the use of "cards" and flexbox to increase the responsiveness of the webpage.  The loss of panels and wells can be easily replaced by cards. 

### [AngularJS 1.6.9](https://angularjs.org/)
The use of angular in this project is primarily to abstract some of the extra code away from the base.  Partials have been included for bootstrap headers, navigation, and the table itself.  The partial table worked fine on my localhost, however it failed to load on a windows server.  I believe this is because of the order of loading.  We need the HTML to build BEFORE the datatables take over onload.  I may need to move the 
   _example-html-table.html back into the index page. 
  
### [Datatables 1.10.18](https://www.datatables.net/)
As of November 2018, this is the most recent version of datatables.  
- There are some issues with the exporting of excel files while using IE. 
- Former functionality for ColVis that included check boxes has been removed from the datatables build. 
- If it is is not already in this version. I am adding checkboxes back into the ColumnVisibility buttons.
- I also like my export functionality to be available in drop down.  Right now I am at a cross between jQueryUI and Bootstrap for my drop down buttons. 

### [FontAwesome 5 (free)](https://fontawesome.com/icons?d=gallery&m=free)
FontAwesome has figured out how to monetize their icons by offering a version 5.  There are still many of the same free icons that are prefixed with fas and far instead of version 4's fa.  

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Ruby Rabelle** - *Initial work* - [RubyRabelle](https://github.com/RubyRabelle)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* The folks over at Datatables.net
* Twitter Bootstrap
* Angular JS



