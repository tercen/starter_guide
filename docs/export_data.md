# Export Data Tables

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
