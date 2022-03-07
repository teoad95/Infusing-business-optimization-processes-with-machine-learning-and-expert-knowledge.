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

The datasets contains 50 runs for each possible out of 9 combination of one selection from each row. 

Under datasets folder there are two files:
- **StatisticalDataset**, each row represents a run, contains statistical information for the orders included in the selected run
- **ExtendedStatisticalDataset**, each row represents a run, contains statistical information for the orders included in the selected run and also contains statistical information for the orders that exist in each 1/10 of the input jumbo.


### Experiments

The experiments have been done into a notebook file and it is suggested to run it in google colab. No extra action is necessary to be done. The structure of the experiments is the following:

- Data visualization
- Simple regression experiments using each dataset
- Classification experiments using each dataset
- Exploratory regression experimets using each dataset
- Generalization tests

### Conclusion

- **Statistical vs extended dataset** Experiments using both datasets achieved the goal.  The performance was al-most the same with the statistical dataset to perform slightly better in somecases and the extended statistical to some others.  The extra information passedinto the models,  did not seemed to help them and also made them harder toget explained.  The correlated position of the common fields was not the same,meaning that the models constructed using the second dataset are not the sameas the ones constructed with the first, fed with extra information.  Statisticaldataset’s fields seemed enough to perform predictions
- **ML vs DL** Both using ML and DL the goal achieved.  DL performed better than the MLwhile the second provides easier explainability - interpretability of the results.In case it is not necessary to focus on the explanation of the prediction, or wedo not want to construct a system which will also give suggestion, DL model issuggested to get used, while in the other cases, ML should used.
- **Interpretability** Interpretability  by  its  self  is  a  research  subject.   For  the  experiments  of  thecontext of this thesis, the interpretability only of the machine learning models was examined.  The explanation of the prediction of the models,  increase ourconfidence to use them, and help us to understand how the models work.
- **Generalization** The generalization of the models that achieved the goal tested also by takingadvantage of the way the dataset constructed (table 1).  Out of the six teams ofruns, tries made, by leaving one of them left out, and by training models withthe other five.  The experiments showed that the ones trained with the teamswhich contains reels with lower width values can be good predictor for the oneswith greater values.  Especially when a model gets trained from a combinationof big and small teams it performs better.  Also the normalization of the data,helped the models to generalize better.

### Future work

As future work, the presented work can be extended to:
-- Focus on model’s interpretability - explainability.  Give suggestions for the input in order to reduce the total waste percentage.
-- Construct a reinforcement learning agent which will use any of the alreadyconstructed model’s as a reward function.  This agent will act as a planner
