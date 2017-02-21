# Commit and Branching Guide

When building a piece of software we should strive to follow these principles:

### Staging and Production Branches

Each repo should have two main branches with an infinite lifetime

+ `staging`
+ `master`

These branches should be protected (i.e. no one should be able to push to them and Pull Requests have to be approved by at least one reviewer).

`master` should always be in a *production ready* state

`staging` should reflect a state with the *latest delivered development changes* for the next release. This could also be called "integration branch".

When the source code in the `staging` branch reaches a stable point and is ready to be released, all of the changes should be merged back into master and tagged with a release number (following the [semver](http://semver.org/) pattern).

### Other branches

Other branches can be roughly grouped into three categories

+ `feature`
+ `release`
+ `hotfix`

when adding a new `feature` - branch off from `staging` and be able to merge back into `staging`.

when preparing for a `release` - this must branch off from `staging` and be able to merge back into `staging` and eventually `master`.

when making a `hotfix` - these must branch off from `master` and be able to merge back into `staging`, then `master`.

### References

+ [a successful git branching model](http://nvie.com/posts/a-successful-git-branching-model/)
+ [semver - semantic versioning](http://semver.org/)
