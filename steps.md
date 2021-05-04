# Navigating the Data Science Lifecycle Process

It's important to realize that progress isn't linear in a data science project. Data Science projects are cyclical and experimental in nature. As your understanding of the data and problem increase, you'll often revisit earlier approaches and make adjustments. You may even modify the way you're asking the question to make your outcome more actionable. Because of this, it's possible to jump back and forth between virtually any of the steps. 

However, to keep the documentation simple, we'll document the steps in the order they occur in the process. In practice you'll often jump between steps. As long as you understand what the goal of each step is, moving between the steps should be fairly intuitive.

## 1. Open an Ask Issue

The first step for any project is asking a question. We need to identify what we're actually trying to do and why we need to do it. The Ask issue is where we do this.

In this step, the data science team will collaborate with relevant stakeholders to understand the problem domain and begin to frame the problem as a data science problem.

During this step, you want to capture existing workflows, shortcomings, and potential impact as outlined in the Ask Issue template.

Remember, you don't need to figure out everything at once. Fill out as much as you can. You will continue to update and refine the issue as you progress and your understanding of the problem evolves.

The goal at this point is to create a jumping off point for your work and make sure you're solving the right problem. Once you feel you've established a shared understanding of the problem you'll need to get data.

## Updating the Ask Issue

Throughout the course of solving the problem, you'll learn more about the data and develop a clearer understanding of the problem. As you do, you should update the Ask Issue accordingly. This could include refining scope, identifying additional data sources, changing metrics, etc.

The Ask issue should always reflect the team's current understanding of the problem and solution path.

### Next Steps

- Do background research on the problem
- Collaborate and follow-up with stakeholders
- Open a data issue to get data for the problem

## 2. Open a Data Issue

Once you've defined the problem, you'll need to get data. Either there will be existing datasets that you can use or you'll need to create them. Either way, you'll need to open a data issue to capture the requirements and definition of which data you need and what it's for.

> For each dataset needed to solve a problem, you should link to the Data issues from the Ask issues.

### 2.1 Get the Data

Create a Data Acquisition Issue to load the datasets you need from an existing source. Often times, you'll need to collaborate with other teams to do this. The issue is a great place to do that. Once you've created the initial definition, create a data branch to work on the data pipeline. 

### 2.2 Create the Data
 
Often you'll need to create your own data, either by combining existing datasets in new ways or by creating pipelines to ingest data from new sources. In this case, you should open a Dataset Creation issue to collaborate on defining and creating the new dataset(s). Create a data branch to create the new data pipeline.

### 2.3 Validate the Data

Once you've reviewed the data and validated that it meets your needs, merge the data branch to your collaboration branch and close the issue. You should also be sure to include documentation for all datasets used in the project.

#### Tests and Schemas

It's a good idea to write data validation tests and capture schema definitions as part of this step. This will reduce issues later on and create more clarity for the team.

### Next Steps

- Explore the data
- Create additional documentation
- Update and refine the Ask Issue based on data availability

## 3. Open Explore Issues

In order to solve the problem, you'll need to increase your understanding of the data. The best way to do this is through data exploration.

Open explore issues throughout the project whenever you need to increase your understanding of the data and how it affects the problem. If possible, create a list of questions that you intend to answer ahead of time. This will help keep you focused and prevent exploration from going on indefinitely. If you can't come up with any goals ahead of time, timebox it.

#### Linking Explore Issues 

It's important to link your Explore issues to other issues (Ask, Data, Experiment, etc) to make sure you can find them later. You should link the explore issues based off of which worktype prompted their creation. For example, if you're exploring a dataset that you're getting from another source in order to build the pipeline, the explore issue should be linked to the data. If you're exploring data to figure out what target you should create or to validate assumptions, you should link to your Ask and Experiment issues.

### 3.1 Open an Explore Branch

Open an Explore branch to explore the data and collaborate with others. Capture highlights (e.g. a TLDR) of what you find inside of the Explore issue to that others can get a high-level understanding of what you found. Be sure to link to the Pull Request in the Issue so that others can view your full exploration if needed.

### 3.2 Review and Close

Explore branches don't get merged to the collaboration branches because they are hard to maintain and lead to the repo becoming bloated. Instead, when you're finished with exploration, you can mark the Pull Request for review if you want others on your team to see what you uncovered. Once this is done, close the PR and the associated issue without merging. Update the other issues as appropriate based on your new understanding of the data.

If there is critical information uncovered in an an explore issue, then the resolving action should be updating the documentation.

### 3.3 Refactor Useful Components

Often during exploration, you'll uncover useful examples or create utility functions that will have persistent value. If so, you should create another issue and feature branch to add new code or documentation in the collaboration branch.

### Next Steps

- Update the Ask Issue
- Do more exploration
- Refine/fix the data
- Get more data
- Start an experiment
- Add tests to your code
- Refactor useful components created during exploration
- Update documentation based on new understanding

## 4. Open Experiment Issues

Once you understand the problem and the data, you'll want to start experimenting with various approaches to solving the problem. This will involve creating targets, features, models, custom scoring metrics, etc.

For each approach you try, you'll want to create an Experiment Issue. This will enable you and your team to keep track of the various approaches and what the outcomes were.

By creating branches for each experiment, we can isolate the experiments from each other and collaborate together on experiments.

As you create pieces of useful, reusable code (metrics, scorers, features, etc), you'll want to create new feature branches so that you can merge them to the collaboration branch so that you and others can use them in future experiments.

### Next Steps:

#### If Failed:

1. Write a TLDR describing the outcome and why it failed
1. Mark the experiment as failed using a label
1. Close the pull request and experiment issue without merging
1. Update the ask issue accordingly

Then:

- Try more experiments
- Update the data
- Explore the data
- Refine the Ask Issue


#### If Succeeded:

1. Update the experiment issue with a TLDR and mark as successful using a label.
1. Open a Model Issue to prepare the model and pipelines for production.
2. Create a "Model" branch using Main as the base.
3. Merge upstream changes from Main into your experiment branch and resolve any conflicts.
4. Change the target of the Experiment PR to the Model branch.
5. Merge the pull request to your Model branch and close the Experiment Issue.
6. Delete the experiment branch after merging the PR.

## 5. Open a Model Issue

When you've had a successful experiment, you'll want to deploy it. Open a model issue to keep track of all the required steps for deployment. This may include:

- Refactoring the features so they reflect the requirements of the production environment
- Write tests for features, models, and datasets
- Register and package model for deployment
- Deploy and test full ml pipeline against full training data
- Test model performance and robustness
- Add monitoring and logging
- Create release plan (e.g. A/B testing, rollback strategy) and model retraining plan

> As your team matures, you can begin to automate more of these steps using CI/CD and MLOps.

## 6. Repeat

Keep iterating and switching between these steps until you've solved the problem and you have the solution running in production.

## Next Steps

- [Review Branching Strategy](./branching/branch-types.md)
- [Review Issue Types](./issue-types/0-overview-issue-types.md)
