# Jude and Salome - Sustainability, Cost and Stability of the MOFs

CIFs_to_refcode_list.py

Used to convert a folder of CIF files returned from screening processes into a .GCD file containing a list of MOF refcodes that can be input into the CSD_reader.py code.

CSD_reader.py

Contains functions f_to_str(formula) and write_annotations(annotation_csv_path, comps, metal_list).
Reads in file of MOF refcodes and outputs data about the relevent MOFs into two seperate files: MOFdata.csv, containing structural data, and compositional_data.csv, containing elemental compositions.
