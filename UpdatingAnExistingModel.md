# Updating an existing current entity model.

Firstly it is important to note that once an entity model is current we can only change the contents of the entity model file. We can no longer change the meaning of a file. Should we specify that the establishment field refers to a school establishment we cannot update the entity model to instead refer to business establishments. Its meaning is fixed. This is why it is important to get this right the first time. Should you wish to change the name of the entity then the current one would have to be retired to the [/model/retired](/model/retired) folder following the [how to retire an existing model](RetireAnExistingModel.md) instructions and a new model be created.

## Current Model

In order to update a current entity model please do as follows:

1.  Create a new branch named after the entity model to be updated. You can only update one entity model per branch. The branch should be named as follows:

    Update + *entity name*. for Shellfish this would look like UpdateShellfish, for start date UpdateStartDate this should be written in [Camel case](https://en.wikipedia.org/wiki/Camel_case)

2.  Update the entity model in question within the branch. As said above you can change the contents of the file but not its meaning. You can also not change the name of the entity model in this way.

3.  Create a pull request to merge the updated model back into master. This pull request must be approved by **more than one** other members of the data team.
4.  Once enough members of the data team have approved the update the pull request should be merged and the branch deleted.

## Draft Model
This is not required in order to update a draft entity model as these can be updated on an adhoc basis as they are still Work in progress

## Retired Model
A retired model cannot be updated.
