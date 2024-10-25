# Get Started with Tercen

---

## Introduction

This tutorial explains how to navigate the Tercen interface and teaches basic skills for data analysis using Tercen. 

### Topics Covered
- Navigate Tercen
- Upload Data
- Build an analysis Workflows
- Project and visualise data in the crosstab screen
- Perform calculations on data
- Export graphs and data tables.

Note: Right click on a screenshot and open in a new tab if a High Res version is needed.

---

## Video Tutorial
A video tutorial is available at this link. It walks through exercises to illustrate the basic skills for analysing data in Tercen. 
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/932148936?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Get Started With Tercen"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

---

## Navigating Tercen
On log-in to Tercen you will be brought to your Home screen.
![Screenshot](img/Introduction_Home_1.png)

- **Breadcrumb:** A navigation chain. Each link leads to a location in Tercen. Click the home Icon to return to your personal page.
- **Tabs:** Projects, Teams, Team members, and the Activity Log can be accessed here. Blue Text denotes a clickable link.
- **New Project:**  A new project can be created from the Home page or from inside a Team. The creator (Home or Team) is the owner of the project.
- **Search Bar:** Projects, Workflows, Data Tables and Files can be searched. They must be owned by you or a Team you are a member of. Description text is included in the search but not contents of files.


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


### Readme.md
Tercen creates a "Readme" notebook for each project. It is the display page for your project and can contain links to visualisations inside the workflow. The file is created with Markdown a lightweight scripting language.


## Upload Data
Tercen can upload any scientific data and analyse it. This tutorial provides some sample files to explain the concepts.

## Download Tutorial Files
Download the example files from these links.
[Data File](sample_files/Example_Data_File.csv).
[Annotation File](sample_files/Example_Annotation_File.csv).


### Examine the Data
Open Example_Data_File.csv in a spreadsheet program.
![Screenshot](img/starter_guide_data_review_1.jpg)

This data set has 127 Patients where multiple measurements were taken at different time points over the course of the experiment. The data file contains 

- **Factors:** The Column headers of this spreadsheet become **Factors** in Tercen. Factors are "pots" of data (containing everything in the column) that Tercen can project and calculate on.  
- **Identifier Codes:** Unique identifier numbers for Patients, Samples, Experimental Conditions and many other elements. These ID codes are used to protect anonymity and link to Meta Data files with further information on that element. 
- **Experimental Data:** Ordinary information. This file contains some patient data (AGE, RACEGRP, SEX) some experiment data (PANEL_TYPE, MEASUREMANT_TYPE, CELL SUBSET) 
- **Measurement:** A data a file can have one or more measurement to be plotted in graphs. Identifying the Main Measurement is an important concept as analysis usually starts with this and expands from there. 



### Uploading Data
Press the **New Data Set** button. 


Tercen uploads data files using importers. They are specific to the file type being uploaded. Our example file is a CSV file (.csv). Search for CSV, select it and press ok.

Tags can be pressed to filter options in a search.

