# Jude and Salomé - Sustainability, Cost and Stability of the MOFs


 - CIFs_to_refcode_list.py

Used to convert a folder of CIF files returned from screening processes into a .GCD file containing a list of MOF refcodes that can be input into the CSD_reader.py code.


 - CSD_reader.py

Contains functions f_to_str(formula) and write_annotations(annotation_csv_path, comps, metal_list).
Reads in file of MOF refcodes and outputs data about the relevent MOFs into two seperate files: MOFdata.csv, containing structural data, and compositional_data.csv, containing elemental compositions.


 - mof_score_generator.ip

Reads in files of the periodic table (with cost, supply risk, toxicity and radiactivity of each elements) and the compositional_data.csv to create a dataframe containning the cost ($/kg), supply risk, toxicity and radioactivity of the MOFs (saves the file as mof_score_indexed.csv). It uses the chemical composition of each MOF in compositional_data.csv. It creates dictionaries that are then converted into one dataframe.


 - Plots.ip

Reads in mof_score_indexed.csv file to plot various graphs:
Price vs refcode, log(Price) vs refcode, Supply risk vs refcode
log(Price) vs Supply risk, coloured according to Toxicity (a colour scale is indicated to show which MOFs are the most toxic)
log(Price) vs Average Coordination Number, coloured according to Toxicity (a colour scale is indicated to show which MOFs are the most toxic)
Produces a dataframe containing the best MOFs on these criteria (the less toxic, non-radioactive, less expensive, lower supply risk, higher coodination number)

- DATA folder

Contains the output data and generated csv files used for analysis. Only the 2556 pre-selected MOFs (based of void volume for the adsorbed gas, selected by Weronika and Adam) were used for analysis.

-- refcodes.gcd

The refcodes of the 2556 pre-selected MOFs. 

-- mof_data.csv

Identifier, formula, density, mass of the 2556 pre-selected MOFs.

-- compositional_data.csv

Elemental composition of each MOF and percentage weight of each element. Generated from mof_data.csv.

-- pt.csv

Price, Supply risk, Radioactivity and Toxicity of each element in the periodic table.

Supply risk data from the Element Scarcity – EuChemS Periodic Table (https://www.euchems.eu/euchems-periodic-table/).

Price data from various websites providing updated prices for chemical elements (some are daily updates, some are less recent prices).

Toxicity is 1 for the most toxic elements, and 0 for elements considered as non-toxic.

Radioactive elements are given the score of 1, non-radioactive elements the score of 0.

-- mof_score_indexed.csv

File containing the Index,	Price ($/kg),	Supply risk,	Radioactivity and	Toxicity of all 2556 MOFs. Generated from pt.csv and compositional_data.csv.

All those factors take into account the percentage weight of the elements in the MOFs. For example, a MOF containing more Cu atoms will be given a higher toxicity score.

-- mof_score_indexed_density.csv

File containing the Index,	Price ($/kg),	Supply risk,	Radioactivity,	Toxicity, log(Price),	Density and	Average Coordination Number of all 2556 MOFs. 
