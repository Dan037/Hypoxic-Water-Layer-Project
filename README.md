# Hypoxic-Water-Layer-Project
2019/03/12

# Introduction:

This Python code creates a graph of the shallowest depth in the ocean where hypoxia occurs versus date. 
Hypoxia is a water condition where there is not enough oxygen dissolved in the ocean for marine life to 
survive. The threshold for low oxygen was defined according to [1], which uses 2mg/l as the critical value, 
and this number was converted to μmol/kg using conversion factors according to [2], resulting in a 
threshold of 62.5μmol/kg. This conversion was necessary because the data used was from an Ocean 
Observatories Initiative dissolved oxygen profiler that reports dissolved oxygen in μmol/kg. It is located 
at 45N, 125W (off the Oregon coast) and operates from about 30m to 500m.

# How to Use This Program:

This link will take the reader to the OOI profiler that provided the data: 

https://ooinet.oceanobservatories.org/data_access/?search=CE09OSPM-WFP01-02-DOFSTK000 

To download the data on the OOI data portal, log into your account for the site. Select the profiler in the 
data catalog (using science, not engineering, data) and either click the download button or go to plotting 
and click "download data".

Once the corresponding dissolved oxygen data has been downloaded (ensure you have enough space for it - the 
files are several MB each), place them in the same folder as the Python notebook code. As long as the files 
are in chronological order, the program will separate the data in them by date, find all the depths which 
have hypoxic oxygen conditions on that date, and plot the shallowest depth for that date. The final output 
is a graph with date on the x-axis and shallowest depth where hypoxia appears for that date on the y-axis. 
This code will run very slowly on less powerful or older computers, so use it at your own risk.

# Sources:

[1] https://coastalscience.noaa.gov/research/stressor-impacts-mitigation/habhrca/hypoxia-program/

[2] https://slgo.ca/app-sgdo/en/docs_reference/variables-unites.html

# Acknowledgements:

Code for changing pyplot figures: https://stackoverflow.com/questions/17109608/change-figure-size-and-
figure-format-in-matplotlib/17109830

Code for labelling x-axis: https://stackoverflow.com/questions/3100985/plot-with-custom-text-for-x-axis-
points

Code for converting from seconds since UNIX Epoch to date/time: 
https://stackoverflow.com/questions/8777753/converting-datetime-date-to-utc-timestamp-in-python

Seconds since 1900-01-01 to start of the UNIX Epoch: https://stackoverflow.com/questions/8805832/number-
of-seconds-from-1st-january-1900-to-start-of-unix-epoch

Making an integer array using Numpy: https://stackoverflow.com/questions/1859864/how-to-create-an-integer-
array-in-python
