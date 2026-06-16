This repository contains the code and resulting tables and visuals of my paper, The Typological Tokenization Tax.
There are five folders:

1. Code: the python code that I used to assemble data, perform analysis using my pipeline, and create visuals.
2. Tables: the raw data, formatted as .csv files. Most tables were simply used for data assembly or creating charts. The full_language_data.csv table contains all relevant data.
3. Visuals: the visuals created by my python code which were used in the paper
4. flores_datasets: this folder contains the actual corpora used for analysis. The FLORES-200 dataset contains parallel data from 200 langauges.
5. grambank: this folder contains the grambank dataset. This was used to assemble topological data about each language. Due to the large size of the dataset, that folder was not specifically included. However, all relevant topological information for this paper is contained within the full_language_data.csv file. The grambanks questions within the file are listed under their indexes, which each start with "GB". A 1 in the file indicates the attribute is present, a 0 indicates it is not present. To find descriptions of each typological attribute, view the feature_importance.csv file

__In order to best understand the raw data used in this paper, I suggest looking at the visuals, glancing at the files in the flores_datasets folder, skimming the full_language_data.csv file, and finally glancing at the actual code if you are interested.__
The code files perform the following functions:
 - flores_import.ipynb imports the FLORES-200 dataset
 - load_language_resource_levels.ipynb imports the resource levels of the languages
 - morpheme_analysis.ipynb loads the grambank dataset
 - Tokenizer.ipynb performs the tokenization of the multilingual corpus
 - data_combiner.ipynb combines the raw data gathered by the other files, fits the gradient boosting model, and creates graphs to model the data
