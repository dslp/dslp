# Ask Issues

Ask issues are for capturing, scoping, and refining the value-based problems your team is trying to solve. They serve as a live definition of work for your projects and will be the anchor for coordinating the rest of the work you do.

By having the definition of work be in an issue, data science teams can collaborate with their business partners and domain experts to refine and rescope the issue as they learn more about the problem.

You should link to the other issues inside of the Ask issue. This will give people context around why a particular issue is being worked on.

As your understanding of the problem evolves you should update your ask issue accordingly. In order to create clarity, you should be as specific as possible and resolve ambiguities by updating the Ask.

## Anatomy of an Ask Issue

### Problem Statement

The problem statement is a high level description of what you're trying to solve and why. It should be clear what value solving this problem will create and should also set a clear scope for what is and isn't included as part of the problem. 

> If there is a large project with several components, it may make sense to create several Ask issues that link back to a parent Ask Issue.

#### Desired Outcome

This describes what the end state should look like. If it helps, you can think of this as a user story. "I want [persona] to be able to do [action] so that [some outcome] can happen". The goal here is to make sure that your model maps to a business process. The last thing you want is to build out a solution and not have a way to deploy it.

The most important part of this section is to capture what about the existing process will change if your project is successful.

#### Current State

One of the best ways to figure out what you need to build is by understanding the shortcomings of the existing process. You should also capture why the current state needs to change. By focusing on this, you can separate "nice-to-have" projects from "need-to-have" projects and maximize your chances of get your project properly resourced.

### Success Criteria

It's important to know what constitutes success early on in the project. This prevents you from falling into the situation where you've built something that is good from a technical perspective but that the stakeholders reject for some reason. Set clear guidelines and acceptance criteria. If it's not clear what those are, you should do some analysis to figure it out and then verify that with the stakeholders.

#### Impact

Impact is making it obvious what the value of your project will be once done. The more concrete you can make this the better. If you are able to estimate the impact of your project in terms of clear metrics, you'll make it easy for your stakeholders to make a go/no-go decision. 

You should also try to quantify how much of an improvement is needed for the project to be valuable. If a project needs accuracy that is not acheivable using SOTA techniques, it's good to know that before you start working on it.

#### Metrics

Metrics take our impact and convert them into tangible metrics that we can focus on while building our project. This can include both business metrics as well as technical metrics.

For example, if the goal is to improve customer retention, you should define how churn is measured and how you intend measure the improvement. You may also need to capture secondary metrics such as cost of keeping a customer.

Eventually, you'll need to convert your key metrics into technical ones. You should be clear with which ones you're using. For example, if you're doing a classification problem, you should be clear whether you're using accuracy, F-score, AUC, etc. and why.

Finally, you may want to include counterbalance metrics. For example, if your goal is to increase returns while minimizing risk.

#### Constraints

You should capture any constraints your project needs to keep in mind. Ask yourself, what could keep my project from getting deployed. If you think of something, that's a constraint. Some examples include:

- If you need real-time predictions you need a model that can do fast inference.
- Certain data may not be acceptable for use in a model (e.g. privacy or legal constraints).
- Model must have interpretability metrics in order to be acted upon.

### Solution Architecture

It's often useful to document your solution architecture. This can be done using any tool (PowerPoint, Visio, hand-draw diagrams, etc.) 

Including a diagram can be very helpful in understanding how a solution will be implemented. This helps you catch design issues early in the process while the cost to change them is still low.

By doing this throughout the project you'll also be able to see how your solution evolved through time.

Finally, it makes it easier for people who are new to a project to understand what's going on. This means there are lower barriers to collaboration when you need to involve new teams.

### Data Requirements

You should capture which datasets are needed to solve a problem. Include links to the data issues for each dataset (if there are multiple data issues for a dataset, use the most current version. GitHub will track changes to the issue over time, so you can see if the linked issue changed if necessary).

#### Datasets

For each dataset, link to a data issue that describes what's in the data. You can also link to the docs for a given dataset.

> Examples: 
> Customer Transaction History (link to issue/docs)  
> Customer demographics (link to issue/docs)
> Product inventories by store (link to issue/docs)

### Understanding and Exploration

This section is for linking to explore issues that inform the problem. You should also link to relevant docs that help frame the problem.

### Approaches and Experiments

This section is for linking to your experiment issues. This section should essentially be a running log of all the experiments attempted for the ask. Experiments should be roughly chronological. Successful experiments should be listed first.

### See Also

#### Background Info

This is useful for linking to related research, examples you found online, etc. If something is relevant long term (i.e. after the ask is closed), you may want to consider adding it to the docs.

#### Related Projects

Similar to Background info. If there are related projects or repos, you can link to them here. If something is relevant long term (i.e. after the ask is closed), you may want to consider adding it to the docs.
