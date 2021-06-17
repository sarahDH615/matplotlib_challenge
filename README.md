# matplotlib_challenge

![Test tubes with coloured liquids](/images/testTubes.jpg)

### contains:
pymaceuticals_starter_edited.ipynb 

### description:
This pandas file contains analysis done on data from a study on mice with squamous cell carinoma, treated with various drug regimens over 45 days. The study was sponsored by a company producing the drug Capomulin, with the purpose of comparing that drug with other treatments. To that end, this file includes the following:
* Observations about the number of measurements per drug regimen, final average tumor volume of four leading cancer treatments, potential outliers, and possible correlations between mouse weight and average tumor volume.
* Data Cleaning:
    * Merging two datasets into a new dataframe (merged_df).
    * Looking at the tumor values at the start of the study: they are all 45 mm3.
    *  Renaming the 'Timepoint' column to better reflect what it represents (days).
    * Checking the number of mice in the merged_df.
    * Creating a new dataframe (no_dups_df) that has no duplicate rows within a mouse ID.
    * Printing how many measurements are taken at each time point (no_dups_df.value_counts()).
    * Printing the information on the mouse ID that had duplicate values.
    * Comparing the number of mice in the original dataframe    (merged_df) and the cleaned dataframe (no_dups_df) to ensure that only duplicate values, and not all the data for a mouse, got deleted.
* Summary statistics table: divided by drug regimen, using two methods of generating summary statistics (groupby and .agg)
* Total Number of Measurements For Each Drug Regimen:
    * Bar charts showing the total number of measurements taken for each drug regimen, once using plt.plot, and the other using pd.df.plot)
    * Printing the lowest and highest number of measurements taken per drug regimen, and some summary statistics, to observe the range of measurements taken, and average value.
* Distribution of male/female mice in the study: creating pie charts (done twice: once using plt.plot, and the other using pd.df.plot)
* Quartiles and Potential Outliers for Final Average Tumor Volume:
    * Creating a new dataframe (top_regimes_df) that holds only the measurements taken for the final timepoint of each mouse ID.
    * Printing the number of values taken per timepoint for each drug regimen.
    * Printing the mouse IDs that have same final tumor volume as the start value for all mouse IDs: they all have the final timepoint of zero, meaning no measurements were taken for those mouse IDs after the starting timepoint.
    * Creating separate dataframes for each of the four top drug regimens (ca_df, ra_df, in_df, ce_df), and for each dataframe, printing:
        * the different final timepoints and the number of times they appear within the dataframe
        * the contents of the dataframe
        * the average of all the values that are for timepoint 45 (the timepoint at which the study ended)
    * Calculating the quartiles, upper and lower bounds for outliers, and identifying and potential outliers.
    * Creating a boxplot with all of the four regimens, with any outliers as bright red circles.
* Tumor Value over Time for Arbitrary Mouse in Capomulin Regimen: generating a line plot for a randomly chosen mouse ID in the Capomulin regimen, showing the progression of its tumor volume.
* Average Final Tumor Volume vs. Mouse Weight: creating a scatter plot for each drug regimen, showing final average tumor volume of all mice on each drug, based on their weight class, with a linear regression graphed on top of each one. The graphs beside the one for Capomulin are done in order to see whether it is possible to draw out any distinctive qualities in the Capomulin graph by comparison.


