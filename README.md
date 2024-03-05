# JRCustomFunctions

## Description

Jasper Report is an open source Java reporting tool that can write to a variety of targets such as:

- screen
- a printer
- into PDF
- HTML
- CSV
- Excel
- RTF
- ODT
- XSL
- XML

## Introduction

### JRXML Files

You can make JasperReports using xml format on files with format called JRXML where you can generated or designed using tools.

### Jaspersoft Studio

You can make JasperReports usingn Jaspersoftstudio (In this guide we going to use the Community edition version). Jaspersoftstudio allow create highly formatted, pixel-perfect designed reports and data visualizations that meet any requirements and can pull from the widest selection of data sources.

### DataSources

On JasperReports we can have many DataSources like:

- JSON
- CSV Files
- Database JDBC Connection
- EJBQL Connection
- Hibernate
- Excel
- MongoDB
- XML
- JNDI

### Expressions

Report expressions are the powerful features of JasperReports, which allow us to display calculated data on a report. Calculated data is the data that is not a static data and is not specifically passed as a report parameter or datasource field.

## Custom Expressions

One way to have custom expressions on our JasperReports is using a Java class, just follow the below steps:

Make JSON file

```json
{
  "user": {
    "name": "Mauricio",
    "lastname": "Pasten",
    "age": 22,
    "profession": "Developer",
    "email": "mauricio.pasten@nicheaim.com",
    "phone": "+52 5538389460",
    "debt": 200,
    "debtCurrency": "MXN",
    "limitCredit": 1000
  }
}
```

- Add data adapter for JSON File

  ![1](.img/1.AddDataAdapter.png)

- Configure JSON Data Adapter

  ![2](.img/2.ConfigJsonDataAdapter.png)

- Make Jasper Report Project

  ![3](.img/3.MakeJRProject.png)

- Add New Report

  ![4](.img/4.AddNewReport.png)

- Save the Report and change the name if you want

  ![5](.img/5.PathNewReport.png)

- Add JSON Data Adapter to the report

  ![6](.img/6.AddJsonDataAdapterToReport.png)

- Select necessary fields

  ![7](.img/7.SelectFields.png)
  ![8](.img/8.SelectedFields.png)

- Select Fields to GroupBy

  ![9](.img/9.SelectFieldsToGroupBy.png)

- Select Finish

  ![10](.img/10.FinishAddReport.png)

- Take the necessary fields and move to the report design

  ![11](.img/11.SelectNecessaryFields.png)

- Make new Java maven project with a custom method for example on this case we add total credit that return the limit fo credit for use.

  ![12](.img/12.MakeMVNProject.png)

- Package your project

  ![13](.img/13.PackageMVNProject.png)

- Make lib directory on Jasper Report Project and then copy the package of your maven application

  ![14](.img/14.MakeLibAndCopyJavaPakcage.png)

- Refresh and then open the Config build path and add the new dir lib

  ![15](.img/15.ConfigureBuildPathAndAddLib.png)

- Add your package form lib to Classpath

  ![16](.img/16.AddToClassPath.png)

- And also add to Orden and Export

  ![17](.img/17.AddToOrderAndExport.png)

- Select the report and go to Properties

  ![18](.img/18.SelectReport.png)
  ![19](.img/19.GoToProperties.png)

- Add your class with custom expression

  ![20](.img/20.AddClass.png)

- Add new text field to use your custom expression

  ![21](.img/21.AddNewTextField.png)

- Press doble click on the left selecting your new text field and open the expresion editor and then use the method that you make and pass the necessary params from your report. Like this

  ![22](.img/22.AddCustomExpressionUsingClass.png)

- And To finish this example just go to preview and see the behavior from the new text field

  ![23](.img/23.Preview.png)
