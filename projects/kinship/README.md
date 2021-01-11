README.md

# Detecting kinship in text

## Overview

This project contains 4 sub-directories:
data
Evaluation
Rules
Extra

These are explained here in turn.

## System

The main kinship detection system is contained in System
The system folder contains the following files:
- control_rule.py
- Rule1.py
- Rule2.py
- Utils.py
- Main.py
To run the system, run main.py. To be able to run the system, make sure Preprocessed_html_data.pkl is in the data folder. Uncommenting the last Iines will output predictions for rule 1 and rule 2 separately and of both rules combined to the data folder. 

## Evaluation

The Evaluation scripts are in Evaluation.
To evaluate, run the cells in evaluate.ipynb. To evaluate, make sure the data folder contains the following four files:
- gold_relations.pkl: this contains a list of relations (as 3-tuples) adapted by hand from https://www.geni.com/projects/Friends-and-Their-Friends/30024
- predictions_rule1.pkl: this contains a list of relations produced by rule 1
- predictions_rule2.pkl: this contains a list of relations produced by rule 2
- predictions_combined_rules.pkl: this contains a list of the relations produced by either rule 1 or rule 2

## data

The data folder contains the following pickle files:
 - Preprocessed_html_data.pkl: this contains a list of 41255 utterance dictionaries from Friends transcripts, taken from https://fangj.github.io/friends/
 - gold_relations.pkl: this contains a list of relations (as 3-tuples) adapted by hand from https://www.geni.com/projects/Friends-and-Their-Friends/30024
 - predictions_rule1.pkl: this contains a list of relations produced by rule 1
 - predictions_rule2.pkl: this contains a list of relations produced by rule 2
 - predictions_combined_rules.pkl: this contains a list of the relations produced by either rule 1 or rule 2

## Extra

The Extra folder contains:
 - Jupyter notebooks containing code used to produce gold_relations.pkl (in the subfolder Building_Relations)C
 - Jupyter notebooks containing code used to process MELD data and create Preprocessed_html_data.pkl (in the subfolder Preprocessing)
 - Jupyter notebook used to extract manual annotation data, and the manual anotations themselves (in the subfolder Manual_Annotating)
 - Rules that weren't used in the final system (in the Old Rules subfolder)
 - data used for various parts, not required by the final system (the data subfolder)
