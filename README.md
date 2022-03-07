# Infusing business optimization processes with machine learning and expert knowledge.

In the context of this work a research on an appliance of ML techniques in a manufacturing optimization problem was done and presented a data driven tool that operates as a decision support alongside with an already developed and existing combinatorial algorithm, for an optimization problem, which minimizes the production waste, given a set of constraints.

The experiments include:

- **Dataset construction** Explore the metadata and construct datasets
- **Problem modelization** Modelize and address the problem both as regression and classification, perform experiments using ML and DL techniques and find the most efficient combination of dataset - modelization.
- **Interpretability** because of some times, it is necessary to be able to explain a prediction, the models interpretability checked.
- **Generalization** because the space of the input is infinite and unfortunately the dataset using which the train will be done cannot describe it perfectly, train and comparison of generalization of models using different sets of the training space will be done.

The questions that answeredd are:

- Which is the best way to modelize the dataset?
- ML or DL and why?
- Can we explain the predictions?
- Which is the best way to construct a dataset? 

### Datasets

Datasets can be found under \Dataset folder. There are 2 different datasets. Both got created using data from a data generator. The rules using which the dataset for the experiments constructed are shown in the following table and we tried to mimic a real production situation.  Each cell represents a category.  For example, A represents the existence of 1-10 reels of 1000-2000width in a run.  The rules using which the data created are:

| Widths/ Number ofreels|1-10|11-40|
|---	|---	|---	|
|1000-2000|A|B|
|2000-3500|C|D|
|3500-5000|E|F|
