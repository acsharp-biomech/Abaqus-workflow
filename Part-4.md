# Part 4
## Setting up a job
Now that all the materials, BCs and Loads have been assigned, you can set up each Job.

Double click the Jobs tab under Analysis in the model tree. Name your job, select your model and click Continue...

In the next dialog box you can write a description of the job and change some general setting. Leave all the options as the default, but under the Memory tab you may want to change the percentage of physical memory the process will take. 

Now change any of the BC or loads for your particular job. You can suppress or resume BCs to change the bite point (right click the BC for the menu), and you can change the loads in the same way. When you have all the loads and BC set up for your job, right click on the Job and select Write Input. This will write an input file to your working directory that you can run later in a batch file. Alternatively, if you just want to run one job, you can click Submit. You can also Data Check first for any errors. 

Create more Jobs, change the loads and BCs and write an input file for each different simulation. 
## Running your Jobs from a batch file
If you have a series of Jobs it is faster and easier to run as a batch file from the command line. You do not need the Abaqus user interface open for this.

To write a batch file, open any text editor and type:

*call abaqus j=Job-1 int ask_delete=off*

*call abaqus j=Job-2 int ask_delete=off*

*call abaqus j=Job-3 int ask_delete=off*

Replace Job-1, Job-2 etc. with the name of the input file you saved your jobs as. Save the file as runAbaqusJobs.bat (or whatever you want, but it's important it's saved as a .bat NOT .txt) in the same directory as the input files.

Open your command line by searching cmd in the start menu.

Change the directory to the working directory you saved the input files, and the batch file to:

*cd "C:\...\AbaqusWD"*

Then run the batch file you wrote earlier by typing:

*runAbaqusJobs.bat*

This will call each input file in succession so you can go home and relax :)

