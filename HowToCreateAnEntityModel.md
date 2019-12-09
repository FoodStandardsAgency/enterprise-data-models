# How to create an entity model


#### Creating the entity model file
When creating an entity model you should start by creating a copy of the [template file](/model/template.md). This file should be named according to the entity to be modeled. i.e. the shellfish entity model should be called shellfish.md

This file should be saved under [/model/draft](/model/draft) should a file already exist by the same name as the one you wish to create then an entity model is already a work in progress for this entity and that one should be updated instead. **There should only be one entity model for each entity** This lack of duplication extends to [/model/current](/model/current) as well as just the draft folder. If you wish to update an existing model in [/model/current](/model/current) then please follow the [updating an existing model instructions](/UpdatingAnExistingModel.md) Once you have made and renamed a copy of the template file please push this to the master branch

### Writing the draft entity model.

Writing the entity model is as simple as filling out the file which you already created. All fields should be filled in when possible and to the best of your abilities. When an entity is already in use in another system it is strongly advised to involve the owners of that system in the creation of the entity model. **All entity models must be submitted as a draft before becoming current.** Please note an entity model is describing the idea of the identity not an example of it.

The information that should be captured under each subheading can be found in the [entitymodel.md](/EntityModel.md) file. Should there be nothing relevant for capture in a field then that heading can be removed from the file. Please ensure that what is written in this file is valid markdown. The [linter](https://atom.io/packages/linter) and [linter-markdown](https://atom.io/packages/linter-markdown) packages for atom can help with this by highlighting any incorrect syntax.

Once the draft entity model has been created it should be pushed to the master branch within this repository. This can be done directly in the case of a new draft, or via a pull request when updating an existing draft for which you were not the original author.

Entity models in the draft folder can be updated as often as wanted both in terms of meaning and contents.

### Moving a draft entity model to current.
Once happy with an existing entity model it needs to move to current in order for it to be usable. This must be done using a pull request following the process bellow. In order for an entity model to be added to current it must have existed in drafts.
1.   Create a new branch named after the entity model. the name should follow the following scheme:

  current + *entity name*. for Shellfish this would look like CurrentShellfish, for start date CurrentStartDate this should be written in [Camel case](https://en.wikipedia.org/wiki/Camel_case)

2.  Copy the entity in question from [/model/draft](/model/draft) to [/model/current](/model/current) do not make any changes to the file. If updates need to be made to the entity model make them in the draft folder before moving them. The pull request to move the entity model to current must also remove it from draft.

3.  Push your branch to origin if this was done locally.

4.  Create a pull request to merge your changes into master adding at least one other member of the data team to the pull request as a reviewer.

5.  Once the pull request has been approved by another member of the data team merge the request and delete the branch.
