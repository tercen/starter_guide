# Tutorial

---

## Introduction

This tutorial teaches the basic skills features and techniques to begin using Tercen for data analysis.

### Topics Covered

- Navigate Tercen
- Upload Data
- Build an analysis Workflows
- Project and visualise data in the crosstab screen
- Perform calculations on data
- Export graphs and data tables.

_Note: Right click on a screenshot and open in a new tab to see a High Res version._

---

## Navigating Tercen

On log-in to Tercen you will be brought to your Home screen.
![Screenshot](img/Introduction_Home_1.png)

- **Breadcrumb:** A navigation chain. Each link leads to a location in Tercen. Click the home Icon to return to your personal page.
- **Tabs:** Projects, Teams, Team members, and the Activity Log can be accessed here. Blue Text denotes a clickable link.
- **New Project:**  A new project can be created from the Home page or from inside a Team. The creator (Home or Team) is the owner of the project.
- **Search Bar:** Projects, Workflows, Data Tables and Files can be searched. They must be owned by you or a Team you are a member of. Description text is included in the search but not contents of files.

---

## Create a Project

![Screenshot](img/starter_guide_new_project_1.png)

Press the New Project button to create one.

- **Name:** The project name
- **Description:** This description will appear on screen. The search bar will look for keywords in this section.
- **Visibility Setting:** Public means anybody on the Tercen server can see it.

The project will be visible in the **Explore** section of Tercen.
Unchecking the setting means only the owner (Person or Team) can see it .

A project is a repository for the elements of a data analysis. It contains Data Tables, Files and workflows.
![Screenshot](img/starter_guide_new_project_2.png)

### Header

- **Lock Icon:** Closed = Project is private.  Open = Project is public.
- **Activities Tab:** Activity log for this project.

### Control Bar

- **New Data Set:** The default method to Upload data files to Tercen.  
- **New Workflow:** Create a data analysis pipeline.
- **New file:** Create a text file for notes.
- **Upload file:** Upload non-data files to the project.
- **Upload workflow:** Upload a workflow which was exported from another project.
- **Project Settings:** Change Name, Description or Privacy Settings.
- **Clone Project:** Make a copy of this project for a new user or team. Anything with a clone icon can be copied to one of your projects or teams.

---

## Upload Data

Tercen can upload any scientific data and analyse it. This tutorial provides some sample files to explain the concepts.

### Download Tutorial Files

Download the example file from this link.
[Data File](sample_files/Example_Data_File.csv).

### Examine the Data

Open Example_Data_File.csv in a spreadsheet program.
![Screenshot](img/starter_guide_data_review_1.jpg)

This data set has 127 Patients where multiple measurements were taken at different time points over the course of the experiment. The data file contains

- **Factors:** Column headers of a spreadsheet become Factor names in Tercen. Factors are "pots" of data (containing everything in the column) that Tercen can project and calculate on.  
- **Identifier Codes:** Unique identifier numbers for Patients, Samples, Experimental Conditions and many other elements. These ID codes are used to protect anonymity and link to Meta Data files with further information on that element.
- **Experimental Data:** Ordinary information. This file contains some patient data (AGE, RACEGRP, SEX) some experiment data (PANEL_TYPE, MEASUREMANT_TYPE, CELL SUBSET)
- **Measurement:** A data a file can have one or more measurement to be plotted in graphs. Identifying the Main Measurement is an important concept as analysis usually starts with this and expands from there.

---

### Upload to Tercen

Tercen uploads data files using importers. They are specific to the file type being uploaded.

Press the **New Data Set** button.

![Screenshot](img/starter_guide_data_upload_1.jpg)

Our example file is a CSV file (.csv).

Search for CSV, select it and press Next.

Tags can be pressed to filter options in the search.

Use Drag and drop from your file browser or the browse button to select Example_Data_File.csv.

![Screenshot](img/starter_guide_data_upload_2.jpg)

Press Next to upload it.

When Tercen uploads files it converts them to a Dynamic Table.

Dynamic Tables allow Tercen to perform calculations and mix data from incompatible file types.

---

## Analyse Data with a Workflow

Workflows are pipelines that process data, perform calculations on it, make visualisations and create reports.

Press the **New workflow** button

Name the workflow. (for example "Example Workflow")

Press **Next**

![alt text](img/starter_guide_workflow_1.jpg)

_Note: Pre-defined workflows can be selected. These are called Templates. Templates are used to standardise pipelines to perform routine analysis or ensure repeatability by following the same analysis steps for each experiment._

The Workflow Canvas will load.

![Screenshot](img/starter_guide_workflow_2.jpg)

- **Save:** Will turn orange when there is a change to save.
- **Run All:** Runs each step in the workflow sequentially until all have completed or failed.
- **Reset** Unlocks a run-completed workflow so it can be modified.
- **Add Step** Add an independent Step to the workflow. Use this to start a pipeline.
- **Clone** Takes a copy of the workflow and recreates it in a different project.
- **Size Control** Adjust zoom view of the canvas.

### Table Step

Start a pipeline by pressing the **Add Step** button.

![Screenshot](img/starter_guide_workflow_3.jpg)

Choose the **Table** Step and press Ok

![alt text](img/starter_guide_workflow_4.jpg)

Select the uploaded **Example_Data_File.csv** file from **Current Project** and press Ok.

_Note: Data Tables uploaded to the Main Library of Tercen are available to every project on the server. Normally these are reference data sets for calibration._

The data table is loaded to the workflow canvas. Extend the pipeline by clicking the step to bring up the **Local Toolbar**.

![Screenshot](img/starter_guide_workflow_5.jpg)

- **Reset:** Resets this step and any dependent steps in the pipeline. Previous steps are not reset.
- **Edit:** Opens this step to expose its features and settings.
- **Rename:** Change the step name.
- **Delete:** Removes the step.
- **Duplicate:** Makes a copy of the step linked to the same previous data.
- **Add:** Adds a new step, downstream from this step.
- **Status Indicator:** Green when that Data Step has run successfully. Red if there is a problem.

### Data Step

Press the **Add** button.

Choose the **Data Step** option and press Ok.

![alt text](img/starter_guide_workflow_6.jpg)

The Data Step will open automatically.

Data Steps are the main engine blocks of analysis in Tercen. Visualizations and Calculations are set up and performed here.

![Screenshot](img/starter_guide_Data_Step_1.jpg)

- **Control Bar:** Features for data manipulation and visualisation.
- **Factors Panel:** Factors from the data file appear at the beginning of this list. As the pipeline is built folders are added containing the new factors that are created by the calculations it makes. Each Data Step has access to the factors of the steps that precede it in the pipeline.
- **Crosstab Grid:** Factors are dropped onto this grid to make projections. These projections create the base data set that is used to create visualisations or perform calculations.

### Make an X-Y Axis projection

Drag VALUE out of the Factors panel with your mouse.

The areas it can be dropped will go green.

![Screenshot](img/starter_guide_Data_Step_2.jpg)

The crosstab grid will offer an X-Axis and a Y-Axis, which project numbers.

It will offer Row and Column which are used to form groupings of the data in the X-Y Axes.

We recommend that you always start a projection with your main measurement in the Y-Axis.

Drop VALUE on the Y-Axis.

The crosstab builds a Data Cell with all the measurements in the VALUE factor ordered from lowest to highest.

![Screenshot](img/starter_guide_Data_Step_3.jpg)

_Note: Unlike a spreadsheet data cell, a Tercen data cell can hold multiple data points. This is an important concept that impacts how a calculation or visualisation is performed._

Drag CELL_SUBSET to X-Axis to make a simple projection.

Grab the black lines of the crosstab grid and drag them out to make the data more visible.

Hold the **CTRL** key on your keyboard and scroll with the mouse wheel to zoom in and zoom out.

![Screenshot](img/starter_guide_Data_Step_4.jpg)

Press Save and return to the workflow canvas by clicking the breadcrumb.

Click the data Step to bring up the Local toolbar and rename this Data Step to "Simple Projection".

Save the workflow.

### Make a Row/Column projection

Click the Data Table and add a new Data Step from the Local Toolbar.

When Factors are dropped to columns or Rows the crosstab will split the data cell into groups of data points according to that factor. These new data cells have their own X-Y Axis.

Multiple Factors can be dropped to Rows and Columns forming sub groups. A black line will appear either side of a Row or Column indicating whether a Factor will be dropped before or after the existing one.

Groupings on a Crosstab projection work from Outside to In. For Columns, the topmost factor is grouped first, and then sub-groups in order below it. For Rows, the leftmost factor is grouped first, and then subsequent factors working to the right.

Make the following projection.

> VALUE to Y-Axis.  
> SEX to Column.  
> AGE to Column (after SEX).  
> CELL_SUBSET to Row.  
> PANEL_TYPE to Row (before CELL_SUBSET).  

![Screenshot](img/starter_guide_Data_Step_5.jpg)

Save the Data Step.

### Make a Heatmap

The Control Bar has buttons and Zones to control how a projection is visualized.

- **Buttons:** Apply a pre-defined change to the data such as point size, style, or clear the grid.
- **Zones:** Light up green and apply a change to the data that is defined by the Factor that is dropped onto it. These are Filters, Colors, Labels, and Error Bar.

Adjust the projection as follows.
> SUBJECT_ID to Column (After AGE).  
> VALUE to Colors.  

The crosstab grid now has one data cell per measurement and they are coloured according to their VALUE with low numbers trending towards blue and high numbers trending towards Red.

Press the Style button and change it from **Point** to **Heatmap**.

Take a moment to move the black lines and zoom in to examine the data. Try to look for immunological patterns.

![Screenshot](img/starter_guide_Data_Step_6.jpg)

Save the Data Step, return to the workflow canvas and rename the data step "Heatmap".

Grab Data Steps and move them on the canvas with your mouse.

![Screenshot](img/starter_guide_workflow_7.jpg)

### Adjust the Colour Palette

Tercen has colour control options for visualisations made with the crosstab.

Right Click on the data cell to bring up the menu.

Select **Palette**

Experiment with the choices on offer.

### Take a Snapshot

Tercen can take a quick snapshot of the visualisation in the crosstab grid and export it as a **.png** image file.

Press the **Download** button to export the heatmap.

_Note: This feature will only export what it sees on screen. If the crosstab is longer than the bottom of your screen those parts will not be imaged. Adjust the black lines to get a better image or follow the tutorial to learn how to use the Plot operator._

---

## Working with Operators

Operators are computer programs written in common languages such as R or Python. They perform calculations or visualisations on data and can be simple or complex depending on their design.

Tercen provides hundreds of standard operators to choose from, and your organisation may have created an operator specific to your labs process.

### Add an Operator to a workflow

To add an operator to your pipeline click the Data Table and select **Add** from the local toolbar.

Use the Operator Tag to filter and search for **Mean and SD** and press **OK**

A Data Step will open with the Mean and SD Operator loaded.

This operator will calculate a Mean and a Standard Deviation for every data cell.

![Screenshot](img/starter_guide_operator_1.jpg)

- **Plus Button:** Add an operator into an existing step.
- **Name and Version:** The name of the operator and a version number 0.0.0 which links to instructions on how to use it.
- **Minus Button:** Removes the operator.
- **Run Button:** Locks the projection in the crosstab and runs the operator code on the data.

### Set up an operator

Operators receive data from the crosstab projection but they need the projection to be configured according to their internal design or they will not run properly.

To discover the projection an Operator expects, click on the version number link under the operators name.

This will take you to the operators GitHub page where layout instructions will be available in the README file.

![Screenshot](img/starter_guide_operator_2.jpg)

- **Description:** Explains what the operators function is.
- **Input:** Specifies the crosstab projection that is required by the Operator.
    _Input Zone:_ The crosstab zone a factor can be placed in.
    _Factor Type:_ Operators may need a numeric or text input.
    _Status:_ Whether this zone must contain a factor or can be optionally left blank.
    _Description:_ Additional information to help pick an appropriate factor for this operator to get meaningful results.
- **Output:** Describes the outputs the Operator will create.
    _Factor Name:_ The name of the new factors that will be created by the operator to hold the results of its calculations.
    _Factor Type:_ What type of data the new factors will have such as numeric or text.
    _Calculation:_ When the operator runs it will perform one calculation per defined group. These can be Cell, Row, Column or Whole Crosstab.
    _Description:_ A description of what the new factor is.

According to the specification the **Mean and SD** expects the main measurement (VALUE in our example file) to be placed on the Y-Axis. It will make two calculations on every cell, A Mean and a Standard Deviation and will create two new factors **mean** and **sd** to hold the results.

Go back to Tercen and drag **VALUE** to the **Y-Axis**.

### Run an Operator

Press the **Run Button** to start the operator. Some buttons in the Operator Panel will change

![Screenshot](img/starter_guide_operator_3.jpg)

- **Reset Button:** The run button will change to a reset button when the code is finished. It must be used before any changes to the projection or re-runs of the operator.
- **Result Button:** Displays the results of a calculation or any specialised visualisation to generated.

Press the **Result Button** to review a data table with the results of the operator.

![Screenshot](img/starter_guide_operator_4.jpg)

The operator created two new factors **mean** and **sd** according to the spec. There is one calculation for each as there was one Data Cell in the projection.

_Note: Tercen automatically creates a **namespace** prefix to prevent duplicate Factor names from being created. They are based on the Object Type. For example Data Steps generate "ds1." "ds2." and so on. Other steps have different namespaces.

Add some groups to the projection.

Press the **Reset Button** to unlock the projection and drag the following.
> CELL_SUBSET to Row.  
> SEX to Column.  

Run the operator again and check the results.

Now there is a Mean and a Standard Deviation calculated for all 118 cells (2 x Columns, 59 x Rows) in the Crosstab.

Save the Data Step and return to the Workflow Canvas.

### Project the results of an Operator

_Note: The Status Indicator on the  Mean and SD data step should be green._

To access the results of an operators calculations add a new data step to the Mean and SD using the Local Toolbar.

_Note: The Tercen AI will attempt to automatically create a projection from a Data Step above. For the purpose of this tutorial we will reject the suggestions and build each projection manually._

Press the **Clear** Button to re-set the crosstab grid.

The Factors Panel has two folders. One with the Factors from the data file and one with the new factors created by the Mean and SD operator.

Make this projection.
> mean to Y-Axis.  
> CELL_SUBSET to X-Axis.  
> CELL_SUBSET to Colors.  
> Graph Style Button to Bar.  

![Screenshot](img/starter_guide_operator_5.jpg)

Save the Data step

Return to the Workflow Canvas

Rename the Data Step to "Bar Graphs"

### Plot Operator

Operators can generate visualisations as well as new Factors. To get more comprehensive and featureful graphs use the plot operator.

Add a Data Step to **Mean and SD** using the Local Toolbar

Use the Operators tag and Search to find the **Plot** operator.

When the Data Step opens. Clear the crosstab grid

Make the following projection.
> mean to Y-Axis.  
> CELL_SUBSET to Row.  
> SEX to X-Axis.  
> SEX to Colors.  
> sd to Error Bar.  
> Graph Style Button to Bar.  

![Screenshot](img/starter_guide_operator_6.jpg)

Operators can have settings which define parameters to modify how they process data. The settings are accessed by changing from **Factors** in the panel window to **Settings**.

The Plot operator settings define export file type, image sizes, labels for data and more.

Each setting has a tooltip icon (?) with information on how to set parameters.

Find and set the following parameters.
> xlab to Patient Group.  
> ylab to Cell Type.  
> title to Mean and SD Graph.  
> theme to classic.  

Press the **Run** Button.

![Screenshot](img/starter_guide_operator_7.jpg)

Images are rendered using standard Bioinformatics protocols as defined by the _ggplot_ R package.

They can be downloaded individually by clicking the relevant link.

Or scroll to the end of the page and batch downloaded all images in a ZIP file.

Save rename the Data Step and return to the workflow canvas.

### Workflow Report Panel

The Plot operator passes its results into the Workflow report panel.

![Screenshot](img/starter_guide_operator_8.jpg)

This panel can build up a comprehensive report from all the Plot Operators in the workflow.

---

## Join

Tercen can combine data files and form a relational database inside your workflow.

### What is a Join

Databases relate information with codes called "keys". In simple terms, a "key" is a match made between two tables because they both contain a column that has the same data in it.
There are many practical "keys" in a typical biology experiment. Obvious examples are Patient ID or Sample ID.

Earlier, when we checked our file, we saw it had the identification codes SUBJECT_ID and EXPERIMENT_ID.

Download the [Annotation File](sample_files/Example_Annotation_File.csv) from this link.

Open it with a spreadsheet.
![Screenshot](img/starter_guide_Join_1.jpg)

The file contains some drug condition information for our experiment. Notice it also has a Factor called EXPERIMENT_ID. This is the key we will use to join our example files.

_Tutorial Midpoint Test: Upload the Annotation file to your project and add it to the workflow canvas._

### Joining Tables

Click the Example_Annotation_File table on the workflow and add a Join from the Local Toolbar.
_Note: Select a RightTable if your Files location on the workflow canvas is to the right of the one you want to join to and LeftTable if it is to the left._

You will see a Join step has two nodes at the top, and one is already connected to your annotation file.

Click the free node on the top of the Join and then click the bottom node of the Example Data File table.

![Screenshot](img/starter_guide_Join_2.jpg)

Edit the Join step.

The Factors of each table are displayed side by side. Matching two together forms a key for the data.

Choose EXPERIMENT_ID from each table and click the Run Step button.

### Check a Join

Add data step to the Join.

Project the factors you picked for the **key** into the crosstab rows.

> EXPERIMENT_ID (From Example_Data_File.csv) to Row.  
> EXPERIMENT_ID (From Join) to Row.  

The crosstab will show all of the matches it has made.

If the Join column is blank you will know that the key has failed.

![Screenshot](img/starter_guide_Join_4.jpg)

Return to the workflow canvas and rename the step to "Join Check"

### Project from a Join

Now that the data files are joined we can project from both and use the annotation file go provide extra context to the Example date.

Add a Data Step to the Join.

Make the following projection.
_From Example Data File_
> VALUE to Y-Axis.  
> PANEL_TYPE to Row.  
_From Join_
> Treatment to Column.  

![alt text](img/starter_guide_Join_5.jpg)

Save the Data Step and rename it to "Condition".

---

## Export Data Tables

Tercen can use projections to build curated data sets out of factors from uploaded tables and calculations made by operators. These can be Exported easily and can be very useful for extracting simple data from complex files, perhaps for input to a downstream process.

Add a new Data Step to the **Mean and SD** step using the local toolbar.

Clear the grid.

Make the following projection.
> CELL_SUBSET to Row.  
> mean to Row.  
> sd to Row.  

_Note: Building an Export Table is one of the rare cases where the Y-Axis is not used._

Press the **Tables** Button to view the data in the projection.

![Screenshot](img/starter_guide_export_1.jpg)

Go to the **Rows** tab

Select **Download**

A CSV file of the data will be created and downloaded to your desktop.

Save the Data Step. Return to the Workflow Canvas and Rename it "Export Table."

---

## Gather

Until this point in the tutorial we have used a file with a single **Main Measurement** called VALUE. We have expressed the importance of using the Main Measurement on the Y-Axis and followed this principle with all of our examples.

But what if a file has more than one main measurement?

An operator may specify a Main Measurement on the Y-Axis and if your file has more than one measurement and it will be necessary to convert from Wide Format to Long Format.

The difference between wide data and long data is an important Data Analysis concept.

**Wide Data** is the traditional table format that you would see in a spreadsheet. Rows are individuals and columns tell you information about that individual. We get to a piece of information by visually cross referencing the row and column. Wide data is easy for humans to read but is difficult for computers to read.

**Long Data** is a list format with one piece of information (measurement) per row and the descriptive information for the piece is repeated as many times as needed. Computers work faster with lists, they do not get bored reading the same information over and over again.

The conversion process to change wide format to long format is called a **Gather**.

### Examine the Data File

Download the [Example_Multi_Measurement_File](sample_files/Example_Multi_Measurement_File.xlsx) from this link.

Open it in your spreadsheet software.

![Screenshot](img/starter_guide_Gather_1.jpg)

This is a traditional Wide Format data file.

There is an identifier codes (SUBJECT_ID, event_id).
Some experimental data (AGE,SEX,DATE).
And multiple measurements (CCR7, CD3, CD45, CD8, CXCR3, FSC-A, HLADR, IgD, PD-1, SSC-A, TCRgd).

Click the **Before Gather** tab in the spreadsheet.

The top three lines of the spreadsheet are colour coded.

![Screenshot](img/starter_guide_Gather_2.jpg)

- **Yellow:** Factor names for id codes and experimental data
- **Green:** Factor names for measurements
- **Blue, Beige, Orange:** Individual records with data.

Click the **After Gather** tab on the spreadsheet.

![Screenshot](img/starter_guide_Gather_3.jpg)

Each measurement has moved to an individual row and its column header becomes a label used to describe it.
The non-measurement data column headers are repeated as many times as needed on every row.

Note that two new Factor names (in purple) are created.

- **variable:** For the group of labels.
- **value:** For the group of measurements.

### Gather Data in Tercen

Upload the Example_Multi_Measurement_File.xlsx to your project and add it to the workflow canvas.

_Note: This file is an Excel file. Remember to look for the correct importer._

Add a **Gather** Step from the local toolbar.

![Screenshot](img/starter_guide_Gather_4.jpg)

Open the Gather step.

![Screenshot](img/starter_guide_Gather_5.jpg)

Use the plus buttons to add the channel factors to the list to be gathered

Leave SUBJECT_ID, AGE and event_id to be un-gathered. They will be repeated on every row.

Click the **Run Step** button.

_Note: You may be wondering why SEX and DATE don't appear in the list. The factors are separated into Numeric and Character as text data can't form a main measurement._

### Projecting Gathered Data

Add a Data Step to the Gather from the local toolbar.

The new Factors **variable** and **value** have been created and we can project value as a group and use variable to interpret it.

Make this projection.
_From Gather_
> Value to Y-Axis.  
> Variable to Row.  

This gives an advantage for making graphs because multi-variate plots are now possible.

Add to the projection.
_From Example Data File_
> SSC-A to X-Axis

Tercen will build a bi-variate plot of SSC-A against each of the gathered channels.

![Screenshot](img/starter_guide_Gather_6.jpg)

---

## Filter

Filters are a way of narrowing down the data projected in the crosstab grid.

Use them to control what is shown in a graph or sent to an operator for calculation.

Tercen Filters use "Boolean Logic" which is based around the concept that all values are either true or false and by asking enough true/false questions you can get to any data point.

In Tercen a Filter is a list of rules built up in the settings. Each rule has three parts.

- The **Factor** it is based on.
- A **Logic** for the rule to use.
- And a piece of Data to **Define** the rule.

Scroll down our crosstab projection. See there is an irrelevant plot where SSC- A is being compared to itself. Lets create a filter to remove it.

### Create a Filter

Drag **variable** and drop it on the **Filters** Zone.

The Filter screen will open.

Change the name to "Exclude Channels"

To remove the SSC-A channel we will build a rule as follows.
> Variable (Factor)  
> not equals  (Logic)  
> SSC-A (Definition)  

You can use the search icon to find individual data in a factor.

Click OK and check the crosstab projection. SSC-A is gone.

### Create a Filter Range

You can re-open a filter to modify it by clicking the Filter Zone chevron.

Multiple Filters can be created on a projection and filters can be made more complex with multi-line rules.

To exclude outlier values from the projection with a filter range drag **value** to filter.

Call this one “Upper and Lower Bound”

Build this rule.
> value (Factor)  
> greater (Logic)  
> 0 (Definition)  

Press plus to add a line

Build a second rule.
> value (Factor)  
> less (Logic)  
> 10000 (Definition)  

![Screenshot](img/starter_guide_Filter_3.jpg)

Press Ok and check the projection to see how it has changed.

_Note: Be aware that Filters apply their rules from the Top down. The top rule is applied first and then the next one, and so on, down the list. The rules at the top DO affect the rules that come after them.So it is possible for an earlier rule to exclude data that you expect a later filter to operate on._

Return to the workflow canvas and rename the step to "Side Scatter Plots".

---

## Collaborating

Making projects public is a way of collaborating with others. Tercen has some more features which help.

### URL Links

Every location in Tercen has a URL reference. They are shown in the blue text on the breadcrumb and in the activity log. To take a colleague to an exact spot in a project copy the URL and sent it to them. Remember they will need to be a member of your Team to be able to see it.

![Screenshot](img/starter_guide_collaborate_1.jpg)

### Teams

Anybody can create a Team in Tercen.

![Screenshot](img/starter_guide_collaborate_2.jpg)

Members of a Team can be added by their User Name or the email account they used to sign up.

![Screenshot](img/starter_guide_collaborate_3.jpg)

Any projects created while inside the team will be visible to everybody in the team.

![Screenshot](img/starter_guide_collaborate_4.jpg)

### Readme.md

Tercen creates a "Readme" notebook for each project. It is the display page for your project and can contain links to visualisations inside the workflow. The file is created with Markdown a lightweight scripting language.

---

# Alternative Video Tutorial

A video tutorial is available at this link. It walks through exercises to illustrate the basic skills for analysing data in Tercen.
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/932148936?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Get Started With Tercen"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>