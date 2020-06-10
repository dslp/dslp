# The Data Science Lifecycle Process

The Data Science Lifecycle Process is a set of prescriptive steps and best practices to enable data science teams to consistently deliver value. It includes issue templates for common data science work types, a branching strategy that fits the data science development flow, and prescriptive guidance on how to piece together all the various tools and workflows required to make data science work.

## Getting Started

To get started, you can read about the steps [here](steps.md).  
A template repository for projects following this process can be found [here](https://github.com/dslp/dslp-repo-template).  

For more background on what this is and why you should consider adopting it, continue reading below.

## Key Topics

- [Branching Strategy](branching/branch-types.md)
- [Issue Templates](issue-types/0-overview-issue-types.md)
- [Workflows](steps.md)
- [Semantic Version of Data Science Assets](semantic-versioning.md)
- [Labels](labels.md)
- [Standard Repo Structure](https://github.com/dslp/dslp-repo-template)

## Why did we create this and why should you adopt it?

Data Science is hard. Enterprise Data Science is harder. Figuring out how to consistently go from asking a question to delivering a solution is something very few teams and even fewer enterprises have figured out. There have been major steps forward in this space. The proliferation of DataOps and MLOps are standardizing practices for building robust data pipelines and model deployments and tools like AzureML make parts of the data science process significantly simpler.

However, even with these important evolutions, we were still seeing huge gaps in data science teams across the board. Simply put, while many of the solutions solve key problems data science teams face, no one was answering the question, **How do we put this all together into a single workflow?**

This meant everyone was solving these problems from scratch. The Data Science Lifecyle Process is designed to be simple, lightweight, and effective. 

## Key Components

To address this need, we came up up with workflows and prescriptive guidance in several key areas.

### Team Workflows and Orchestration

Providing guidance and best practices on how to coordinate your data science teams, development teams, DevOps teams, and stakeholders. We illustrate how to move between the various phases of the process and make sure everyone stays on the same page.

As data scientists ourselves, we wanted to enable data scientists to work in ways they are used to. On the other hand, we also wanted to give the data science process more rigor and make it easier to integrate with the rest of the organization so that it's easier to push our solutions to production. Our approach represents a bridge between the two.

### Issue Templates

We've created a set of Issue Templates to bring consistency to work and make sure there are clear steps at each step of the process. Read about Issue types [here](issue-types/0-overview-issue-types.md).

### Branching Strategy

The typical GitHub Flow or Git Flow branching strategies are a great starting point, but they don’t lend
themselves to the experimental nature of data science. We created a branching strategy that works for
data science workflows while still being familiar to your development teams. Read about the branch types [here](branching/branch-types.md).

### Artifact Management

We provide guidance on how to track all of your various artifacts including exploratory analysis, experiment logging, serialized models and machine learning pipelines.

#### Examples

- Model registry
- Experiment Logging
- Container Registry
- ML Pipelines

### MLOps

There is a great body of work and set of tools for adopting MLOps. MLOps lets us apply DevOps practices to our training, deployment, monitoring, and retraining processes. We directly integrate the best MLOps practices into the Data Science Lifecycle Process so we can make the most of the developments in this area.

#### Examples

- Versioning models
- Logging and monitoring
- Continuous Deployment and rollback strategy
- A/B Testing
- Automated Retraining

You are of course free to use any component on it's own, but we find it's most effective if you combine everything.

## Design Goals

We designed the DSLP to be:

- Lightweight and easy to adopt
- Flexible and easy to adapt
- Minimally Opinionated

When we say minimally opinionated, we mean we tried to make as few assumptions as possible about:

- Team and organization structure
- Type of problem being solved
- The technologies being used

Where we do make assumptions, we do so where we think the benefits are high and universally applicable.

What this means for you is that you can start adopting the DSLP today without a major disruption to your team. You can also adopt it piecemeal to smooth out the learning curve (which is pretty flat to begin with). Ultimately, we hope that teams will take this as a baseline so that they can focus on creating new value and responding to the needs of their own organizations, instead of spending so much time working on process.
