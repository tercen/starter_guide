# Working with Operators

Operators are computer programs written in common languages such as R or Python. They perform calculations or visualisations on data and can be simple or complex depending on their design.

Tercen provides hundreds of standard operators to choose from, and your organisation may have created an operator specific to your labs process.

## Add an Operator to a workflow

To add an operator to your pipeline click the Data Table and select **Add** from the local toolbar.

Use the Operator Tag to filter and search for **Mean and SD** and press **OK**

A Data Step will open with the Mean and SD Operator loaded.

This operator will calculate a Mean and a Standard Deviation for every data cell.

![Screenshot](img/starter_guide_operator_1.jpg)

- **Plus Button:** Add an operator into an existing step.
- **Name and Version:** The name of the operator and a version number 0.0.0 which links to instructions on how to use it.
- **Minus Button:** Removes the operator.
- **Run Button:** Locks the projection in the crosstab and runs the operator code on the data.

## Set up an operator

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

## Run an Operator

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

## Project the results of an Operator

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

## Plot Operator

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

## Workflow Report Panel

The Plot operator passes its results into the Workflow report panel.

![Screenshot](img/starter_guide_operator_8.jpg)

This panel can build up a comprehensive report from all the Plot Operators in the workflow.
