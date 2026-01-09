# AbDev

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>AbDev: Predictive Modeling for Monoclonal Antibody (mAb) Biophysical Properties</h1>
    <p>AbDev is a comprehensive predictive model package designed for the analysis of 12 critical biophysical properties of monoclonal antibodies (mAbs). This tool combines a deep learning-based tool, DeepSP, and machine learning techniques to provide insights based on the variable regions sequences of mAbs.</p>

<h2>Getting Started</h2>
<p>To utilize AbDev effectively, follow the guidelines outlined below:</p>

<h3>Feature Preparation</h3>
<ol>
    <li><strong>Prepare a CSV File:</strong> Begin by preparing a CSV file named "Sequence_Info.csv" using the format provided in this guide as a reference. This file should contain the variable regions sequences of the mAbs you wish to analyze.</li>
</ol>

<h3>Generating Spatial Properties with DeepSP</h3>
<ol start="2">
    <li><strong>Run the DeepSP Notebook:</strong> Use the "DeepSP.ipynb" notebook file to execute DeepSP, a deep learning-based tool developed by our group. DeepSP is designed to generate 30 spatial properties of mAbs based on their sequences.
        <ul>
            <li>Upon completion, you will obtain a "SAPSCM.csv" file, which contains the spatial properties needed for further analysis.</li>
        </ul>
    </li>
</ol>

<h3>Predicting Biophysical Properties with AbDev</h3>
<ol start="3">
    <li><strong>Run the AbDev Notebook:</strong> Next, execute the "AbDev.ipynb" notebook file. This step will process the features generated in the previous step and produce the "Prediction_Result.csv" file. This file includes predictions for 12 biophysical properties of the analyzed mAbs. Or you can run train.py to obtain the results directly.</li>
</ol>
<h2>NOTE</h2>
<p>AbDev models are sensitive to the version of TensorFlow. Please use version 2.12.0</p>
<h2>Citation</h2>
<ul>
    <li> <strong>Please cite when using DeepSP in your research. </strong>
        L. Kalejaye, I.E. Wu, T. Terry and P.K. Lai, DeepSP: Deep Learning-Based Spatial Properties to Predict Monoclonal Antibody Stability, <i>Comput. Struct. Biotechnol. J.</i>, 23:2220–2229, 2024.
        <br><a href="https://www.csbj.org/article/S2001-0370(24)00173-9/fulltext">Read the DeepSP paper on CSBJ</a>
    </li>
    <li><strong>Please cite when using AbDev in your research. </strong> I.E. Wu, L. Kalejaye and P.K. Lai, "Machine Learning Models for Predicting Monoclonal Antibody Biophysical Properties from Molecular Dynamics Simulations and Deep Learning-based Surface Descriptors", <i>Mol. Pharm</i>, 2024.
    <br><a href="https://pubs.acs.org/doi/10.1021/acs.molpharmaceut.4c00804">Read the AbDev paper on Mol. Pharm</a>
    </li>
</ul>
</body>
</html>
