# Experiment Issues

We often won't solve our problem with the first approach we take. It often takes iterating through many versions before we find something that actually works.

Traditionally, the experimentation phase is a place where data science teams struggle to be able to relay a sense of progress to others. They are trying many approaches, and in fact making progress, but all they can say is "We're still trying to get this model working". 

After the project is over, the various approaches taken usually are forgotten. When a team comes back to try to improve or fix a model later, they often end up wasting time retrying things that failed in the past simply because they don't know that they've already been tried.

Experiment issues are designed to capture each distinct approach taken while trying to solve a problem. By doing so, teams can clearly communicate what they tried and learn from each others efforts. Additionally, they allow us to implement a model review process and decide in a more systematic way which approaches we want to productionalize. This allows us to catch problems early, - before we invest time in making our models production ready.

The Experiment issues are the pivot point between the exploratory iterative part of the data science process and the more linear model deployment and MLOps portion of the process. 

Once we create a successful experiment, we can validate our approach with others and then elevate it to a [Model issue](5-model-issues.md) and begin the MLOps cycle.

## What to include

Similar to [Explore issues](3-explore-issues.md), experiment issues should contain a TLDR of what was tried and what the outcome was.

All experiments should be linked to an [Ask issue](1-ask-issues.md). Additionally, if using a model and experimentation tracking system (like [AzureML](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-track-experiments)), they should link to the system of record for your experiments. This lets people have full insight into the full experiment lifecycle including what problem the experiment was attempting to solve, what was tried, what combinations of parameters were used, etc.