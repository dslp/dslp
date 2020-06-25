# Semantic Versioning for Data Science Assets

Semantic versioning is super helpful in software projects and allows teams and consumers of apps to keep track of changes and manage expectations around how the software should behave. In software, we can do this by giving version numbers to our code and we're all good.

In Data Science, we have to worry not only about the code, but also about the data, the models, and the environments because they can all affect our outputs and results. We want to be able to use semantic versioning for our data science assets too. This is our approach to doing so.

## Models

### Major Versions

There are two primary reasons to increment your model major version.

1. A change to your model's interface (change to input or output schema)
2. Anytime there is concept drift (change in target, major shift in target population or application). 

The rule of thumb here is if you don't feel comfortable comparing performance metrics across models, you need a new version. 

Additionally, if an consumer of your model has to modify their code to use your model, you need a new version.

### Minor Versions

This represents a change to the way your model is constructed or improvements to the model. This could be anything from changing algorithms, changing feature preprocessing, swapping out embeddings/encodings, etc.

This could also include adding new features as long as those features are internal to the model and don't rely on the the clients to provide them at inference time.

### Patch Versions

Patches should be for retraining your model or changing it's weights. For example, if your model had configurable non-learned parameters (e.g. cutoff threshold) and you needed to change that, you would also increment the patch version before deploying. 

This ensures that if something you configure causes your model to behave weirdly, you can align the changes you made to the change in version number which makes it easier to debug and easier to roll back.

## Datasets

### Major Versions

Increment the major version anytime:

- There is a backwards incompatible schema change (this include types)
- Changes to the meaning/definition of a column
- Major changes to the population (ingesting data from a new line of business, combining multiple data systems into one)

### Minor Versions

Increment the minor version when:

- You add new columns
- A column is allowed to take on new values (new item types or categories)
- Change the way a column is calculated, but not it's underlying meaning or representation (e.g. same type, scale, magnitude)

### Patch Versions

For datasets a patch should be used whenever the data pipeline is rerun, but none of the underlying logic has changed.

- Running the data pipeline to add new data (monthly updates)
- Correcting errors in the data without changing meaning or calculations (usually caused by upstream data source issues, not the pipeline itself).
- Performance improvements (in case a performance improvement accidentally breaks something, you can roll it back and revert to a previous version)

### Before 1.0.0 Release

Before the 1.0.0 Release you should use minor versions to denote changes to the meaning of the dataset (new columns, schema changes, new joins, etc) and patch versions for changes to your implementation (change in calculation, grouping mechanisms, etc). Before you release your first version you will change your dataset a lot. In this case you mostly want to communicate when you've added net new functionality to your dataset.

## Environments

### Major Versions

Adding or removing packages or updating dependencies to a major version (e.g. pandas 0.25 to 1.0)

### Minor Versions

If you need to change the minor version of a package or lock versions that were previously unspecified. 
