# Part 5
## Abaqus post processing
To see the results from a job that you have submitted, or ran as a batch file, right click the job and select Results (make sure you have the correct working directory set). This will open the Results tab and display a new model tree on the LHS of the window. You will find the output file in this model tree.

You can change the appearance of the model by clicking ![image](https://user-images.githubusercontent.com/80410515/111640761-6919ca80-87f4-11eb-88f5-5bb18cf888fb.png). This will open a dialog box that gives you the options to change the *Render Style*, *Colour* and the type of *Visible Edges*.

You can also display the deformed ![image](https://user-images.githubusercontent.com/80410515/111640871-82227b80-87f4-11eb-8634-0aa0d1d5327a.png) model or the undeformed model ![image](https://user-images.githubusercontent.com/80410515/111640903-89e22000-87f4-11eb-8e1e-025c9b9b017e.png).

To display the stress or strain contours select the deformed shape ![image](https://user-images.githubusercontent.com/80410515/111640965-9b2b2c80-87f4-11eb-954c-16bcbc54cf5d.png), undeformed shape ![image](https://user-images.githubusercontent.com/80410515/111641000-a41bfe00-87f4-11eb-90c2-6a28fe078fc6.png), or both ![image](https://user-images.githubusercontent.com/80410515/111641027-aa11df00-87f4-11eb-855b-5b8dac764548.png). When displaying contours on both, change the appearance of the undeformed model by clicking ![image](https://user-images.githubusercontent.com/80410515/111641055-b0a05680-87f4-11eb-8825-b4c68e9d2e00.png). 

Change the Contour Plot Options by clicking ![image](https://user-images.githubusercontent.com/80410515/111641094-bbf38200-87f4-11eb-994d-c0d1d10e39dd.png). In the dialog box you will find the maximum and minimum stress, principle strains etc. and the location, and you can change the appearance of the contours (under the *Basic* tab) to Line, Banded or Quilt, and the contour intervals from Discrete to Continuous. Play around...this is all entirely up to you.

At the top toolbar you can change the type of results that are being displayed: stress (S), strain (E), displacement (U), reaction force (RF)...these are probably the only ones you are going to need.

To get the RF from the bite points click ![image](https://user-images.githubusercontent.com/80410515/111641255-e1808b80-87f4-11eb-9ed0-9124edb887c9.png) to probe the nodes. Select *Nodes* in the dropdown list next to Probe and then click on the node for the bite point.

To get the internal strain energy (Ԑ) expand the Output database file in the model tree, expand the History Output and then double click *Strain energy: ALLSE for Whole Model*. A temporary XY plot will appear. Click ![image](https://user-images.githubusercontent.com/80410515/111641366-feb55a00-87f4-11eb-98f4-280e3e09e2ea.png) to probe the plot and click the line near the top.

Export a Field Output Report to get the stress and strain values for every node (and then get mean, median, boxplots etc. in R). Go to the menu Report > field output, and select the components you want to export. In the Setup tab, name your file and uncheck Column totals and Column min/max. The field output file can then be opened in R for analysis. 

Setting up a *View Cut* is easily done by clicking the *Activate/Deactivate View Cut* icon ![image](https://user-images.githubusercontent.com/80410515/111641522-260c2700-87f5-11eb-98c4-0ade515619bc.png). By clicking the next icon across ![image](https://user-images.githubusercontent.com/80410515/111641586-36bc9d00-87f5-11eb-975e-75dd965450c8.png), you can change the axis and location of the cut.

You can also probe ![image](https://user-images.githubusercontent.com/80410515/111641631-3fad6e80-87f5-11eb-88a8-22961947225d.png) nodes or elements on the model for stress or strain values in critical areas of interest. 
