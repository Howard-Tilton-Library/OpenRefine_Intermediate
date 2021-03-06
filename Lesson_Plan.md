# OpenRefine-Intermediate
Intermediate Data Cleaning Using Basic Programming

This will be an introduction to using programming within OpenRefine to edit and enhance data. Bringing your laptop 
with [OpenRefine](http://openrefine.org/download.html) pre-downloaded and your own messy data is recommended. Attendees will 
begin by learning how faceting, sorting, and clustering data can help create cleaner data sets for other uses. This will be
followed by an introduction to the uses of GREL and Jython to edit data, open refine operation code in JSON to simplify repeat 
tasks, and JSON to transform data during export.

Audience: Senior undergraduates, graduate students, lab assistants, staff, and faculty

## Getting Started
How to install OpenRefine: https://github.com/OpenRefine/OpenRefine/wiki/Installation-Instructions

## Beginning a Project
### To create a project 
* Double click openrefine.exe where you saved it on your computer
* A command line box will open and the GUI will open in your default browser
* Select "Create Project" on the left and the location of a project 
  * Select the appropriate type of file to parse data as (tab-delimited text)
  * Experiment with options within that type (character encoding, rows to discard or store)
  * Review the preview to make sure your data is being parsed correctly
  * Select "Create Project>>>" at the top and wait
  * When the project opens, scroll through some of the rows/pages and double check your parsing settings worked
### To exit the program
* CTRL + C will close the command line and stop the program (even if it's still open in your browser)
### To open a project
* Start OpenRefine up again
* Now select "Open Project" to work on the project you've previously created

## Review your Data
### Faceting
* Use the dropdown menu on a field (like Genre) to "Facet>Text facet"
* On the left you can now see the contents of the field, how often those contents repeat, and you can sort

### Edit cells
* Sometimes you will want to edit the contents of a field based on what you see in the facet
* On the genre column, try edit cells > split multi-value cells > by separator (;)
* Refresh the faceting and review the changes

### Edit column
* Use Edit column>Split into several columns on PhysicalDescription
* Split first on ":" and then on ";" to create 3 columns with distinct datasets
* Facet resulting columns
* What do you see?
* You should have types of materials, description of the materials, and size of materials in their own columns
* If you mess up, go to "Undo/Redo" at the top of the left column, and select the nearest step before your mistake, 
then return to "Facet/Filter" and try again

### Clustering
* Facet one of the new final Physical description columns.
* Select "Cluster" in the box or on that column select "Edit cells>Cluster and edit..."
* Experiment with your options until you have joined all of the appropriate values
* How have the results in the facet box changed?

### Using GREL (Google Refine Expression Langauge)
* [GREL](https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Expressions) allows you to use regular expressions to edit in OpenRefine 
* Preview shows results on 10 of your rows...second row shows value after running

### Jython Scripting
* [Jython](https://www.jython.org/) is an open source implementation of the Python programming language, integrated with the Java platform. Jython itself is written in Java and supplemented by the dynamic object-oriented programming features of Python; it allows Python to run on any Java platform.

## Ending a project
### To export a project
* Once your project is open, select the export drop down
* Select the appropriate option:
  * tab or comma-separated value will create the most basic result
  * templating allows you to create records for multiple schema using JSON
  * if your columns are aligned with an RDF schema, you can also export triples
  * to share your entire project (not just your data, but the transformations you completed on it), select export project
* If you save and share a project, the recipient will have to open it in OpenRefine
### To import a project
* Select Import Project in the left side of the screen
* Browse and select the file you saved in the last step
* Rename if necessary, and select "Import Project"
### To reuse project operations
#### To export project operations
* Select Undo/Redo
* Select Extract...
* Select the desired operations and copy the resulting JSON
#### To apply project operations
* Select Undo/Redo
* Select Apply...
* Paste the code from the step above into the box and click "Perform Operations."

## Advanced Options
### Reconciliation
General information about Reconciliation Services in OpenRefine: https://github.com/OpenRefine/OpenRefine/wiki/Reconciliation-Service-API
LCNAF and LCSH reconciliation: https://github.com/cmh2166/lc-reconcile
VIAF reconciliation: http://refine.codefork.com/

* Demo a reconciliation against Wikidata
* Additional reconciliation options exist, and if you've got sufficient programming skills, you can build your own!

## Additional Resources for learning OpenRefine, Regex, Jython and more
1. Guides or Lessons on OpenRefine
* Bolam, Mike. "Cleaning and Linking Data with OpenRefine" (https://mbolam.github.io/DigMitCS_openrefine/) (accessed 7/9/2018)
* Michael, Brinna. "OpenRefine" University of Illinois at Urbana-Champaign Library Libguide (http://guides.library.illinois.edu/openrefine/home) (accessed 4/22/2019)
2. Tools
* [regular expressions 101](https://regex101.com/) (tool for creating and testing regex)
* [Google Refine Cheat Sheets](http://arcadiafalcone.net/GoogleRefineCheatSheets.pdf)
* [Library Carpenty OpenRefine](https://data-lessons.github.io/library-openrefine/07-using-transformations/)
* [OpenRefine GREL recipes](https://github.com/OpenRefine/OpenRefine/wiki/Recipes)

