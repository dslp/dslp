# Explore Issues

A lot of data science is exploratory. The goal of this type of work is to increase your understanding of the data and the problem. Because of this, you really don't care about the code that much. The code is just an means to the end, which is getting more knowledge about the problem. 

Oftentimes, data exploration is only relevant while you're doing the work, or for providing context of why a decision was made.

Traditionally, data science teams have three options here.

1. Don't retain exploratory code in the repo.
2. Retain all exploratory code in the repo
3. Selectively commit exploratory code to the repo. 

The biggest challenge with exploratory work is figuring out when you should merge it? If you merge it, how do you decide when you should deprecate it? How can you ensure your exploration code is reproducible? What does it mean to "test" exploration?

Because it's often more work than it's worth to test exploration code, we should be hesitant to commit it to our main branch.

Additionally, if we merge all of our exploration, we will quickly get notebook sprawl and our repo will be an unreadable, unmaintainable mess.

As an alternative, we can create explore issues and pull requests where we descibe and publish our work. 

Most of the time, it's sufficient to push our code to an explore branch and then close it without merging when we're done. The pull request will still contain all of our code if we need to view it later and by linking our explore issues to our other issues, we'll maintain a historical record without cluttering up our repo.

In the cases where a piece of exploration evolves into something we want to reuse or capture as part of our documentation then we can push changes to our repo to update the docs or add some code to our repository. 

## Linking Explore Issues

Explore issues should be linked to other issues so that they are given context. Often exploration without context of why it was done is not useful.

We should link the explore issues based on what issue prompted them.

For example if you are exploring a new dataset to understand it's properties, you would link to an ask issue. If we're trying to validate assumptions or learn more about our target population, you would link to either an Ask or Explore issues. There are no hard rules here. The idea is you want to create a clear history and give other context about why an certain explore issue was created.
