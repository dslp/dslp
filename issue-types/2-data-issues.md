# Data Issues

Data issues are for defining the requirements and acceptance criteria of a dataset needed for a problem. You should create one Data Issue *per version of a dataset*. Once a dataset is validated and accepted, you should publish that dataset as a version. For further changes and updates, you should create new Data Issues. This allows you to clearly mark milestones for when a dataset is done and creates clear expectations for the team on what's in their data.

## Data Acquisition

Data Acquisition issues allow the data science team to collaborate with the team that owns the data to define which parts of the data they need inside the issue.

They also enable a data review process to ensure that the data being loaded is what is needed for the problem at hand.


Examples:
- Loading tables from a data warehouse to build models
- Loading customer transcript text files from the enterprise data lake
- Loading records from your company's CRM
  
> The more explicit you are about defining data requirements and writing validation tests, the less time you'll have to spend fixing your datasets later on.
> Writing data validation tests is a great way to protect against breaking changes when you push updates to your datasets.

## Dataset Creation

In contrast to the data acquisition issues, data creation issues usually require a lot more experimentation and prototyping before a final dataset is ready to merge.

The goal of this issue is to collaborate on creating the dataset you need. It will be completed once you've created and validated a data pipeline and created documentation for the new dataset.
