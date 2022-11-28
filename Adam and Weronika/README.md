# Adam and Weronika - Pre-selection of the MOFs + Widom insertion simulations

#### Non-disordered_MOF_subset.gcd
The list of refcodes of all 87929 non-disordered MOFs, obtained from CSD database.

#### Preselection.ipynb
Python script used for the pre-selection of MOFs - excluding the MOFs with a zero void volume to create the VOID_MOFs.gcd list, and then computing the window sizes for all 26040 structures contained there, excluding the ones with a zero window size, and creating three output directories: a new directory of cif files for use in further calculations, dictionary of MOF names and their window sizes, and a a text file containing the names of MOFs which returned the "Error processing message". 

#### VOID_MOFs.gcd
The list of refcodes of all non-disordered MOFs containing an accessible void volume.

#### Window Sizes Graph.ipynb
Python code used to plot histograms of window sizes. 

#### CoRe Database Analysis.ipynb
Python script used to analyse the CoRe database, match the entries with the list of Large Window MOFs, and obtain the desired CIF files. 

#### CoRe_Large_MOFs.zip
Directory containing all CoRe MOFs containing the appropriate window sizes.

#### Data analysis.ipynb
Python script used to analyse the data - reading in the output file, calculating selectivities and associated errors, plotting the histograms of selectivity values and identifying the most selective MOF structures.

#### Final_results.csv
CSV file containing all the final results: Henry's coefficients, selectivities and associated errors.
