# Success Measurement of New Work using bibliometric analysis  
This repository contains the data and code used in the paper "Success Measurement of New Work using bibliometric analysis".
Further, this repository serves as a demonstration of bibliometric analysis using Python and free to use data sources.

## Data
Data is sourced from Scopus [https://www.scopus.com/search/form.uri?display=advanced]. A institutional login is required to access the search.
Scopus allows to export the search results as a BibTeX file. We exported BibTeX including all the possible metadata. In order to get the refenrece data in a format where we can work with it, the data must be exported as a CSV file.
The data is stored is the 'data' folder as 'scopusXX.bib' and 'scopusXX.csv'. XX represents the number of the query used for the search. The query is also visible in the analysis notebook.

### Transformation attempts
Since the BibTeX export does not contain the raw refenrence data but only a link to the references on Scopus, we attempted to transform the BibTeX file to include the reference data.
The transformation results are stored in the 'data_transformed' folder. The number refers to the query used for the search.
However, while the transformed file seems OK at first glance, the tool used for the analysis is not able to read the file correctly. The reason for this is not clear yet.
The tool is available to use in the 'tools/transform.ipynb' notebook. The same environment as for the analysis is required.

## Code/Analysis
The requirements for the code are stored in the 'requirements.txt' file.
The code is stored in the 'analysis' folder. The code is written in Jupyter Notebook format.

The main tool used for the analysis is 'PyBibX' [https://github.com/Valdecy/pybibx]. All information on how to setup and use the tool can be found in their repository.
We have prepared two notebook templates for our purposes.
The first one is 'analysis_template.ipynb'. This notebook contains most of the general analysis methods that PyBibX offers.
The second one is 'demo_analysis_template.ipynb'. This notebook is a condensed version of the first one and includes only the most important methods for our analysis.

## How to use
1. Clone the repository and setup the environment using the 'requirements.txt' file. Pyhton 3.12 is recommended
2. Export data from Scopus as BibTeX
3. Copy the template notebook to the 'analysis' folder and rename it to 'analysis_XX.ipynb'. XX represents the number of the query used for the search.
4. Change the parameters in the notebook to match the source data
5. Run the notebook