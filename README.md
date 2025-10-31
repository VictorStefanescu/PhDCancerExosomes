Load libraries/import modules 
Set file paths for import, and output folder directory to save results in 
Create list to store file stats (median averages, quartiles), dictionary to collect speed measurements by treatment type.
Pulse time = 15 mins
Open TAR archive of (file downloaded from paper - 28 BED files in a tar folder - unzipped), extract files to temp folder in python
loop through each gzip compressed BED file and extract useful data - genomic co-ordinates, replication speeds, treatment type - tabular format with columns/rows etc...
Fork speed formula - fork_length_bp = end_positions - start_positions || fork_speed_kb_per_min = fork_length_bp / PULSE_TIME_MIN / 1000
QC - remove artefacts and technical errors
SAMPLE TREATMENT ID BY FILENAME, parses file names for identifers HU, ATRi,
FORK DIRECTION ID BY FILENAME, parses file names for direction identifiers - left or right
BIOLOGICAL REPLICATE, CELL TYPE BY FILENAME
Store file statistics in master list, record sample_name, treamtent, median speed, number of forks detected
Convert master list to csv format so can survey later
Group all files by treatment types, sum forks, averages by median speed across files
Histogram plot - showing distribution of EACH fork speed across each treatment, with red line for median
Boxplot - summary comparison of which treatments cause slowest/fastest replication speeds. Box drawn from Q1-Q3 with red line as median
Output files saved to home directory  
  
