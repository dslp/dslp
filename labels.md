# Using Labels

To help us keep track of our work, we've also created a series of labels for the project. The label definitions are kept in the `.github/labels.yaml' file of the repository. The labels are designed to categorize our work and mark the status. You are encouraged to create your own labels as well, but it is recommended to use the included labels as prescribed so that they are consistent across projects and teams.

## Issue Type Labels

Issue type labels are automatically applied to Issues when created using the correct issue template. They make it easy for your team to see at a glance what type of work item a particular issue is. This also makes it easy to find all the various asks, experiments, and data work streams that are happening.

### Ask

This is applied by default to all Ask issues. By labeling all Ask issues, we can quickly see what high-level problems the team is trying to solve, which helps put the other work in context.

### Explore

This is applied by default to all Explore issues.

### Experiment

This is applied by default to all Experiment issues. This makes it easy to keep track of all the experiment attempts that may be going on in parallel on your team.

### Data

This is applied by default to all Data issues. There should be one Data issue for each version of a dataset. This makes it easy to keep track of which datasets are in flight, and who is working on them.

### Model

This is applied by default to all Model issues. This gives you an easy way to see which models have moved beyond the experimentation phase and into the build phase.

### Deploy

This label is used in conjunction with Model Issues and labels and is used to mark when a model issue has matured to the point of being ready to kick-off the deployment process.

### Communicate

Label used for issues related to creating docs and reports.

## Status Labels

### succeeded

Applied to experiment and model issues when they've met all acceptance criteria.

### failed

Applied to experiment and model issues when they've failed acceptance criteria.

### on hold

Sometimes, work gets deprioritized. Use this label to mark approaches that neither succeeded nor failed.


### blocked - need access

Often in a data science project, you're blocked because you don't have access to something. This could be data, a compute environment, a deployment environment, etc. This happens so often that we created a label for it.
