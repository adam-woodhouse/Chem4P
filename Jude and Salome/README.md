# Jude and Salomé - Sustainability, Cost and Stability of the MOFs


**CIFs_to_refcode_list.py
**
Used to convert a folder of CIF files returned from screening processes into a .GCD file containing a list of MOF refcodes that can be input into the CSD_reader.py code.

CSD_reader.py

Contains functions f_to_str(formula) and write_annotations(annotation_csv_path, comps, metal_list).
Reads in file of MOF refcodes and outputs data about the relevent MOFs into two seperate files: MOFdata.csv, containing structural data, and compositional_data.csv, containing elemental compositions.

mof_score_generator.ip

Reads in files of the periodic table (with cost, supply risk, toxicity and radiactivity of each elements) and the compositional_data.csv to create a dataframe containning the cost ($/kg), supply risk, toxicity and radioactivity of the MOFs (saves the file as mof_score_indexed.csv). It uses the chemical composition of each MOF in compositional_data.csv. It creates dictionaries that are then converted into one dataframe.

Plots.ip

Reads in mof_score_indexed.csv file to plot various graphs:
Price vs refcode, log(Price) vs refcode, Supply risk vs refcode
log(Price) vs Supply risk, coloured according to Toxicity (a colour scale is indicated to show which MOFs are the most toxic)
log(Price) vs Average Coordination Number, coloured according to Toxicity (a colour scale is indicated to show which MOFs are the most toxic)

Produces a dataframe containing the best MOFs on these criteria (the less toxic, non-radioactive, less expensive, lower supply risk, higher coodination number)

