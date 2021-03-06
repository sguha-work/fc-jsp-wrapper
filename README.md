# FusionCharts JSP Wrapper

### What is FusionCharts JSP wrapper?

FusionCharts Suite XT uses JavaScript to generate charts in the browser. Where using this JSP server side wrapper you can create charts in your JSP website without writing any Javascript code. 

### How does the wrapper work?
Charts are generated in the browsers with the help of JavaScript and the HTML code.
Using this JSP wrapper we can generate the required JavaScript and HTML code as a string in the server. We can put this strings in the page to generate charts.

### Version
1.0


### Installation
 * Include FusionCharts.java file in your project.
 * Start using methods and classes available under **"FusionCharts"**.
 
### Usage
##### Chart Class (FusionCharts)
Represent the FusionCharts class that can be initialized to create a chart.
###### **Constructor parameters:**
Following parameters can be used in the constructor in the order as they are described. Some parameters are optional. This function assumes that you've already included the FusionCharts JavaScript library in your page.

| Parameter | Type | Description |
|:-------|:----------:| :------|
| chartType | `String` | The type of chart that you intend to plot. e.g. "column3D", "column2D" etc.|
|chartId | `String` | Id for the chart, using which it will be recognized in the HTML page. Each chart on the page needs to have a unique Id.|
|chartWidth | `String` | Intended width for the chart (in pixels). e.g. 400|
|chartHeight | `String` | Intended height for the chart (in pixels). e.g. 300|
|chartContainer | `String` | Id for the chart container DOM. e.g. id of div|
|dataFormat | `String` | Type of the data that is given to the chart. e.g. "json", "jsonurl", "xml", "xmlurl"|
|dataSource | `String` | Actual data for the chart. e.g. "{\"chart\":{},\"data\":[{\"label\":\"Jan\",\"value\":\"420000\"}]}"|
|extra | `String` | Events and other attributes if any for the chart. This parameter is optional e.g. "{\"events\": {			\"rendered\": function (e) {alert(\"Chart rendered\");}}}"|


##### Example of constructor
```java
// Without event attribute
FusionCharts lineChart = new FusionCharts(
                        "column2d",// chartType
                        "ex1",// chartId
                        "600","400",// chartWidth, chartHeight
                        "chart",// chartContainer
                        "json",// dataFormat
                        "{\"chart\":{\"caption\":\"Harry\'sSuperMart\",\"subCaption\":\"Top5storesinlastmonthbyrevenue\",\"numberPrefix\":\"$\",\"theme\":\"ocean\"			},			\"data\":			[{\"label\":\"BakersfieldCentral\",\"value\":\"880000\"				},				{\"label\":\"GardenGrooveharbour\",\"value\":\"730000\"				},				{\"label\":\"LosAngelesTopanga\",\"value\":\"590000\"				},				{\"label\":\"Compton-RanchoDom\",\"value\":\"520000\"	},	{\"label\":\"DalyCitySerramonte\",\"value\":\"330000\"	}]}"
                    );
```
```java
// With event attribute
 FusionCharts lineChart = new FusionCharts(
                        "column2d",// chartType
                        "ex1",// chartId
                        "600","400",// chartWidth, chartHeight
                        "chart",// chartContainer
                        "json",// dataFormat
                        "{\"chart\":{\"caption\":\"Harry\'sSuperMart\",\"subCaption\":\"Top5storesinlastmonthbyrevenue\",\"numberPrefix\":\"$\",\"theme\":\"ocean\"			},			\"data\":			[{\"label\":\"BakersfieldCentral\",\"value\":\"880000\"				},				{\"label\":\"GardenGrooveharbour\",\"value\":\"730000\"				},				{\"label\":\"LosAngelesTopanga\",\"value\":\"590000\"				},				{\"label\":\"Compton-RanchoDom\",\"value\":\"520000\"	},	{\"label\":\"DalyCitySerramonte\",\"value\":\"330000\"	}]}",
                        "{\"events\": {			\"rendered\": function (e) {alert(\"Chart rendered\");}}}"
                    );
```
##### Methods under Chart class
###### **Render**
Public method to generate html code for rendering chart. This function assumes that you've already included the FusionCharts JavaScript library in your page.
##### Contributors
Sahasrangshu Guha (https://github.com/sguha-work), Subhasis Ghosal(https://github.com/subhasisghosal)
###License

**FUSIONCHARTS:**

Copyright (c) FusionCharts Technologies LLP  
License Information at [http://www.fusioncharts.com/license](http://www.fusioncharts.com/license)
