# Coupling_decay_experiments_with_spectroscopy
This repository was designed for a study on plant decomposition.

## Data Availability
You can find the *betula* leaf decomposition multispectral imaging data: which is a folder that was compressed and that is called **'data_betula_clay.zip'** at this ()[link]. It contains all the 337 pictures in a .tif format taken during the multispectral imaging.

## Content of the Repository
This repository contains:
1. A *betula* leaf decomposition spectroscopy data, which is a .csv called **'betula_clay_spectral_data.csv'**. It is the result of running the **'Jeti_spectrophotometer_plot_maker.ipynb'** and it is used in the **'Leaf_taphonomy_analysis.Rmd'** for the analysis.
2. A python script to process the multispectral imaging data, which is called **'Leaf_decomposition_pipeline.ipynb'**. It outputs: .tif composite image for both fluorescence and reflectance, progression figures made with the .tif composites, overlays in form of 5x5 grids showing you what the script identified as a leaf and a Petri dish and a .csv file containing the leaf surface plus the average intensity that was measured over the leaf for each measurements.
3. A python script to process the spectral data, which is called **'Jeti_spectrophotometer_plot_maker.ipynb'**. It outputs the following, plots of the spectrophotometry with or without various form of normalization in multiple format, depending of the user's will and a combined .csv file with all the data put together and that can be reused later in the R analysis (here we outputted: **'betula_clay_spectral_data.csv'**)
4. An R Markdown document to realize the statistical analysis and figures of the article, which is called **'Leaf_taphonomy_analysis.Rmd'**.
5. A knitted and cleaned version of **'Leaf_taphonomy_analysis.Rmd'**, called **'Betula_ leaf_taphonomy_analysis.docx'**, to avoid going through all the steps below.

## Guideline on how to Redo the Analysis
Here is the step by step guideline on how to redo the analysis:
1. Download the data and all the other documents from this repository and unzip **'data_betula_clay'**.
2. Open **'Leaf_decomposition_pipeline.ipynb'** and run it specifying the path to your unzipped **'data_betula_clay'**, when the input function requires it. The run time should be around 30-40 minutes depending of your machine. When it is done you might want to check the output by the eye especially for the **'leaf_mask_overlay_grids'** to see how well did the algorithm identified the *betula* leaves and the Petri dish. The rest will be used in the **'Leaf_taphonomy_analysis.Rmd'** later.
3. [Optionnal]: You may try the **'Jeti_spectrophotometer_plot_maker.ipynb'**, if you wish on spectral data obtained with a Jeti spectrophotometer. An interface will appear and guide you trough each steps. However, for clarity we uploaded the **'betula_clay_spectral_data.csv'**, since in the end we redid the figures in the R Markdown. This script is a solid answer to the exportation problem that use to occur with the Jeti spectrophotometer. It is a stable version that accommodate the bug and the not bugged version of the .csv files.
4. Open the **'Leaf_taphonomy_analysis.Rmd'**, there are multiple path at the very top of the document. Make sure to set them accordingly to the comments explanation. Then, make sure you keep the parameters (param) correct: species: "betula", substrate: "clay", and models: "both". then you can simply knit the document, which should take between 3-5 minutes.
5. Congrats, you know have the analysis, feel free to check the diagnostic plots and others in the documentation and tweak it how you wish.

## Supplementary Informations
If you need supplementary information, check inside the documents, as they are well annotated and each step is explained in great detail. Cheers!!
