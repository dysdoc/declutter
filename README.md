# Decluttering Challenge (DeClutter)

In the scope of [DocGen2, the Second Software Documentation Generation Challenge](https://dysdoc.github.io/docgen2/index.html), hosted by [ICSME 2020](https://icsme2020.github.io/index.html).

### Task Description
The goal of the DeClutter challenge is to build an automated tool that can identify unnecessary software 
documentation at the class or file level. For example, a comment saying ```//loop from 1 to N``` just before code implementing 
exactly that is not helpful, and worse, could drift when the underlying code is changed to (N-1) (for example). As such, it is considered as non-informative and labeled as "Non-information = Yes". 
The tool should take in a CSV file in the [described format](https://dysdoc.github.io/docgen2/decluttr-format.html), and output a label for each row as either "Non-information = Yes" for clutter, non-informative comments and "Non-information = No" for non-clutter ones.

### Data Description
Both development and test data are distributed as *CSV with UTF-8 encoding and semicolon as separator*.  in the following format 
“id, type, path_to_file, begin_line, link_to_comment, comment, non-information” 

#### Sample line
```"FR974";"Line";"https://github.com/nnovielli/jabref/blob/master/src/main/java/org/jabref/gui/maintable/CellFactory.java";95;"https://github.com/nnovielli/jabref/blob/master/src/main/java/org/jabref/gui/maintable/CellFactory.java#L95";"icon.setToolTipText(printedViewModel.getLocalization());";"yes"```

The Development dataset [declutter-gold_DevelopmentSet.csv](https://github.com/dysdoc/declutter/blob/master/declutter-gold_DevelopmentSet.csv) contains 1050 rows and the 7 columns described above. 

### Evaluation and Ranking
Tools will be ranked according to commonly accepted text classification scoring, e.g. Accuracy, Precision, Recall, Matthews Correlation. We may also award a prize for the tool which does best in some hitherto unappreciated dimension. DeClutter will be run as automatically as possible, using Kaggle as a leaderboard mechanism. This is a great opportunity for new researchers to get involved in the topic.

Participants (either teams or individuals) will initially have access to the development data only. Later, the unlabelled test data will be released (see the timeline below). After the assessment, the labels for the test data will be released as well. Both development and test data will be extracted from the JabRef project. However, participants might use additional labeled data from other sources in order to develop and implement their systems. Guidelines describing the annotation and providing detailed instructions for participants will be released with the development data.

After submitting the predictions for the test data, participants will be required to provide a *short report* including a brief description of their approach, an illustration of their experiments, in particular techniques and resources used (included additional data used for building the model, if any), and an analysis of their results. Formatting guidelines will be released with the test data.

### How to Participate
We invite the potential participants to register using the [web form](https://forms.gle/jkGKF44Roc51L6ZT6). **Registration is compulsory to participate in the challenge, although it is not binding**. In any case, independently of your registration, you can decide to withdraw from participating by not sending the system results during the evaluation stage. When registering, you will also have the option to subscribe to the Google group we will create to keep participants up to date with the latest news related to the challenge. Participants are encouraged to share comments and questions with the mailing list. The challenge co-chairs will assist you for any potential issues that could be raised.

### Important Dates
Timeline for the DeClutter Challenge
* **15th November 2019:** Development data available to participants
* **20th April 2020:** Test data available, registration closes
* **4th May 2020:** System results due to organizers
* **8th June 2020:** Assessment returned to participants

Report submission deadlines
* **10th July 2020:** Submission deadline for reports
* **24th July 2020:** Notification deadline
* **7th August 2020:** Camera-ready deadline (tentative)
* **September 2020:** [Workshop](https://dysdoc.github.io/docgen2/index.html) co-located with [ICSME 2020](https://icsme2020.github.io/index.html)

### Challenge Chairs
[Nicole Novielli](http://collab.di.uniba.it/nicole/), University of Bari, Italy

[Neil Ernst](http://www.neilernst.net/), University of Victoria, Canada

### Contacts
If you have any questions, please contact the challenge chairs

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />The challenge dataset is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
