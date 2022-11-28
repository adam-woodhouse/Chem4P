# Adam and Weronika - Pre-selection of the MOFs + Widom insertion simulations

#### Non-disordered_MOF_subset.gcd
The list of refcodes of 87929 non-disordered MOFs, obtained from CSD database.

#### Preselection.ipynb
Python script used for the pre-selection of MOFs - excluding the MOFs with a zero void volume to create the VOID_MOFs.gcd list, and then computing the window sizes for the 26040 structures contained there, excluding the ones with a zero window size, and creating three output directories: a new directory of xyz files, a dictionary of MOF names and their window sizes, and a text file containing the names of MOFs which returned the "Error processing message". 

#### VOID_MOFs.gcd
The list of refcodes of 26040 non-disordered MOFs containing an accessible void volume.

#### Dictionary of all window sizes.pickle
A pickle dictionary containing 11576 MOF refcodes and their window sizes computed during pre-selection.

#### Error processing MOFs.txt
Text file containing refcodes of all the MOFs which returned the "Error processing" message during window size calculations.

#### Window Sizes Graph.ipynb
Python code used to plot histograms of window sizes. 

#### Large_Windows_cif_scp.zip  
Directory containing the 3934 cif files of all MOF structures containing at least one window bigger than 3.64 A (kinetic diameter of nitrogen).

#### CoRe Database Analysis.ipynb
Python script used to analyse the CoRe database, to match the entries with the list of Large Windows MOFs, and to obtain the desired CIF files for simulations.

#### CoRe_Large_MOFs.zip
Directory containing all 2556 cif files of CoRe MOFs containing the appropriate window sizes. 

#### Data analysis.ipynb
Python script used to analyse the data - reading in the output file, calculating selectivities and associated errors, plotting the histograms of selectivity values, and identifying the most selective MOF structures.

#### Final_results.csv
CSV file containing all the final results: Henry's coefficients, selectivities and associated errors.
