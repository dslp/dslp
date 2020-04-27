# Model Issues

Once you've completed an experiment and are ready to start the model development and deployment process, you should open a Model issue.

You will use the Model issue to turn your experiment into production-ready, deployable code. This will include adding tests, parametrizing your models, etc.

The Model issue marks the beginning of the MLOps process. As your team matures, you can create CI/CD processes and automation around the Model Issue and its associated PR.

For example, once you've created your production model code with tests, parameters, etc, you can use a pull request to trigger a CI/CD pipeline to train, test, package, deploy, and monitor your model. Once your model monitoring detects that your model performance has dropped, you can automatically create a new model PR to retrain the model and mark it for review by the data science team before triggering an automated deployment process.