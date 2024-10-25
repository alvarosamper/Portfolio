Project Overview
The objective of this project was to automate the processing of orders received by a company from various clients, each using their own format, some in .pdf and others in .xlsx. The goal was to develop a solution capable of extracting the requested items from these different formats. Once the items were extracted, the next step involved building a machine learning model, specifically a Natural Language Processing (NLP) model, to classify each product description into a unique code provided by the company, as each item was associated with a specific code.

Objectives
Data Extraction: Develop a system to extract item data from various formats (PDF and Excel files) used by different clients.
Classification Model: Build an NLP-based machine learning model capable of classifying product descriptions into specific company-provided item codes.
Efficiency Improvement: Ensure that the model could process high volumes of data while maintaining accuracy, allowing human operators to quickly verify items if necessary.
Challenges
High Number of Labels:

The dataset contained over 10,000 unique labels, with many underrepresented. This posed a challenge for training the model effectively, as the distribution of labels was highly imbalanced.
Solution: After testing various approaches, we implemented a strategy to create a "rare categories" group for labels that appeared less than 20 times. This approach was chosen over data augmentation methods, which did not yield reliable results for this dataset of approximately 280,000 entries. Given the nature of the task, this solution was effective, as items identified as "rare" or with a low confidence threshold could be flagged for human review, optimizing the manual verification process.
Data Extraction from Multiple Formats:

Extracting consistent data from a variety of .pdf and .xlsx formats was challenging, as each client had unique order formats.
Solution: Custom scripts were developed to parse and normalize data across different file types, ensuring that extracted information was uniform and ready for further processing.
Project Structure
Data Extraction Module: Scripts to process PDFs and Excel files, standardizing data extraction from various formats.
NLP Model: A multi-label classification model to match product descriptions with item codes, including handling rare categories.
Model Evaluation: Performance metrics and error thresholds to identify items requiring human verification.
Additional Documentation




For more detailed information on the project, refer to the full documentation available in resum.pdf. To see the methodology we used for model selection, please refer to the notebook model-selection.ipynb.



Future Improvements
Enhanced Dataset for Rare Categories: Potential future work could involve further refining the model’s handling of rare categories, potentially by collecting more labeled data for underrepresented items.
Improved Data Extraction Techniques: Ongoing work on improving data extraction from diverse file types may also increase model efficiency and accuracy.
