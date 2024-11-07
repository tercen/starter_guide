# Gather

Until this point in the tutorial we have used a file with a single **Main Measurement** called VALUE. We have expressed the importance of using the Main Measurement on the Y-Axis and followed this principle with all of our examples.

But what if a file has more than one main measurement?

An operator may specify a Main Measurement on the Y-Axis and if your file has more than one measurement and it will be necessary to convert from Wide Format to Long Format.

The difference between wide data and long data is an important Data Analysis concept.

**Wide Data** is the traditional table format that you would see in a spreadsheet. Rows are individuals and columns tell you information about that individual. We get to a piece of information by visually cross referencing the row and column. Wide data is easy for humans to read but is difficult for computers to read.

**Long Data** is a list format with one piece of information (measurement) per row and the descriptive information for the piece is repeated as many times as needed. Computers work faster with lists, they do not get bored reading the same information over and over again.

The conversion process to change wide format to long format is called a **Gather**.

## Examine the Data File

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

## Gather Data in Tercen

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

## Projecting Gathered Data

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
