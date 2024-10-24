BOOKS PROJECT -- Álvaro Samper Sánchez
OBJECTIVES:
We were tasked with the problem of a website that wanted to quickly classify books using a model. As a preliminary step, we set the objective of delivering a quick solution that demonstrated the functionality for future results.

Data Generation: To build the model, we needed to generate data, so we manually accessed a website and gathered the URLs of books. We then created an Excel file that also included the index for our multi-label problem. Afterward, we developed a notebook (generar_csv.ipynb) to generate the CSV file.

NLP Process: With the data collected, we performed an NLP process, including data cleaning and other essential steps. For more details on the process, you can continue reading the summary below or check the article available in this repository.

In this case, we classified the books into eight genres: humor, romance, science fiction, adventure, historical, psychological, war, and horror.

PROJECT STRUCTURE:
First, we accessed the provided website and created an Excel file with the URLs of the books and their corresponding categories. Afterward, we developed a notebook to access the URLs and download the book texts, generating a new dataset (generar_csv.ipynb).

Next, we created another notebook for data preprocessing and cleaning. We tested different resolution strategies, including:

TFIDF (which yielded the best results),
Word2Vec (which we had to discard due to problems caused by the extensive vocabulary in the books), and
Neural networks (which we set aside because we couldn’t establish a reliable model structure for optimization).
Ultimately, we opted to first optimize TFIDF, then apply PCA, and finally fine-tune the Linear SVC algorithm.

FUTURE APPROACH:
Regarding this project, it’s important to mention that it’s still a work in progress and will continue privately for confidentiality reasons.
To improve this initial draft, we need to build a much larger dataset, which is crucial in multi-label cases. Once we have this, we can optimize the project using different strategies. In this draft, I only implemented one strategy to demonstrate the progress of the work.
