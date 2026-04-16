# Creating PRs
This page covers some suggested best practices for pull requests (PRs) or merge requests (MRs).

## Background
When we merge code into existing codebases, we often ask students to use the [fork+pull method](https://reflectoring.io/github-fork-and-pull/) to integrate their changes. This allows for review by advisors and other developers, and it also reinforces best practices used by most companies. 

One of the biggest challenges we see is as follows:
1) A student works on a codebase and makes many different, exciting changes to improve the code.
2) They bundle all these changes in to a branch and submit a PR.
3) The PR has 10+ commits, multiple features, hundreds of lines of code, and takes a long time to test and review.

## Creating the right size PR

To avoid creating PRs that are too big or hard to review, a PR should have the following characteristics:

1) Should be on a branch or branch of your fork with a defined name, eg. "documentation-fix", "new-feature-cuda".
2) Should only contain commits to fix an issue that can be easily reviewed and tested by others.
3) Should have fewer than ~200 lines of code affected.
4) Should limit the number of files affected, especially for code. For source code this might be 1-2 files, especially if the codebase is complex.
    - Documentation that uses figures or screenshots is the exception to this rule.

From the best practices article linked in the Resources, you may want to ask yourself the following questions for a PR:
1) Are there unrelated changes that can be pulled out into a separate PR?
2) Have I kept the focus on a single task?
3) Can I add any explanations that will help the reviewer understand the context?

## Using git-cherry-pick to right-size a PR
If you are asked to update your PR to be more granular, you can use `git cherry pick` to pull specific commits into a separate branch and use that for a smaller PR.

- [Cherry-pick tutorial](https://www.atlassian.com/git/tutorials/cherry-pick)
- [Cherry Pick tutorial 2](https://www.slingacademy.com/article/git-cherry-picking-a-detailed-tutorial-with-examples/)

## Automating review of PRs 

You may be able to use a GitHub action like this [PR size labeler](https://github.com/marketplace/actions/pull-request-auto-size-labeler) to encourage committers to submit appropriately sized and scoped PRs. Note that lines of code (LoC) may be a rough measuremetn for the complexity of a specific PR.

## Resources

- [Best practices for managing pull request size - devto](https://graphite.dev/guides/best-practices-managing-pr-size)
