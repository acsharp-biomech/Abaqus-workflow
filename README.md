# Abaqus-workflow
A general Abaqus workflow for static analysis.

This is a step-by-step protocol to set up a simple, static loading scenario including how to assign material properties, boundary conditions (constraints and loads) and run jobs. There are various ways to set constraints (e.g. single nodes, coupling constraints etc.) and loads, and this protocol provides a couple of examples but by no means is exhaustive and I’m sure there are many other ways to do it! But hopefully this will help you get started. There are also different types of loading scenarios, such as thermal expansion, which are not described here. 

1. [Abaqus Basics](https://github.com/acsharp-biomech/Abaqus-workflow/blob/main/Abaqus-basics.md) - The user interface and basics

2. [Part 1](https://github.com/acsharp-biomech/Abaqus-workflow/blob/main/Part-1.md) - Importing a model, importing a second part, and assigning material properties

3. [Part 2](https://github.com/acsharp-biomech/Abaqus-workflow/blob/main/Part-2.md) - creating an analysis step, creating a Set, a "floating" datum and RP, and a local co-ordinate system

4. [Part 3](https://github.com/acsharp-biomech/Abaqus-workflow/blob/main/Part-3.md) - applying boundary conditions and loads

5. Part 4 - Setting up a job and running jobs from a batch file

6. Part 5 - Abaqus post processing
