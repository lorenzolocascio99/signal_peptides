# Detecting Signal peptides


Proteins synthesized within cells must be transported to specific compartments or organelles. This process is guided by hydrophobic signal peptides (SPs), which serve as "address tags" to direct the proteins to their destinations. Developing a model to predict the presence of these peptides could provide valuable insights into protein functions and interactions, especially when experimental data is limited, and may identify new potential targets.

To tackle this task, two models were tested: the Von Heijne algorithm, based on a position-specific weight matrix (PSWM), and a support vector machine (SVM). Both models were trained, validated using 5-fold cross-validation, and tested on the SignalP-5.0 datasets, utilizing data from the UniProtKB database.

The performance of each model was evaluated using various metrics, including MCC, accuracy, precision, recall, and F1 score. The SVM outperformed the PSWM, achieving an MCC of 0.86 compared to 0.78 for the PSWM.

However, both models showed significant misclassifications, prompting further analysis. Many false positives contained transit peptides and transmembrane alpha helices, structures with hydrophobic properties similar to SPs, which likely led to the errors. In contrast, false negatives had different SP lengths and amino acid compositions compared to the overall dataset. These errors suggest that the models' underlying assumptions contributed to the misclassifications, and that leveraging different features could potentially enhance their performance.
