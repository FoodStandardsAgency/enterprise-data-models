# Retiring an Entity model

Retiring a model is an extreme step to take and should only be performed when absolutely neccessary. In order to retire a model the following must all be true:

*  The Model is not in use anywhere within the FSA ecosystem
*  The model is not expected to return anywhere within the FSA ecosystem
*  Retiring the model which would allow a new model to be created with the same name will not cause confusion for our users.

A model should not be retired without unanimous approval within the data team. Should any of the above conditions not be met the data model cannot be retired.

## How to retire the model.

In order to retire a current entity model please do as follows:

1.  Create a new branch named after the entity model to be Retired. You can only Retire one entity model per branch. The branch should be named as follows:

    Retire + *entity name*. for Shellfish this would look like RetireShellfish, for start date RetireStartDate this should be written in [Camel case](https://en.wikipedia.org/wiki/Camel_case)

2.  Move the entity model in question within the branch from [/model/current](/model/current) to [/model/retired](/model/retired) if no models have yet been retired this folder will need to be created. Should a model have already been retired by the same name please number the model i.e. shellfish1.md, shellfish2.md etc

3.  Update the model in question to add the following header "Model retired date" and "Model Retired Reason" These should be the first entries within the model and **Must** be populated.

3.  Create a pull request to merge the branch back into master. This pull request must be approved by **more than one** other members of the data team.

4.  Once enough members of the data team have approved the update the pull request should be merged and the branch deleted.
