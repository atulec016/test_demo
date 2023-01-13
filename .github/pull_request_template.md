# Description of PR
See the development [workflow](https://github.com/ServiceTransition/CloudInfra/blob/master/CONTRIBUTING.md) for PR best practices.

If one wishes for changes introduced in this PR to be **promoted** to higher environments and those changes include resources *not in terraform/lambda/ansible modules*, indicate that need here.
- For details, please refer to RELEASE [documentation](../RELEASE.md#Promotion-Process).

## Previous Behavior
What was the previous state of the system or process that caused this work to be created?

## New Behavior
What changes are new to the system or process that addresses the behavior described above?

## Tests
Some tests (like `atlantis plan`) have to be done after PRs are submitted. In those cases, start the PR with a `[WIP]` title (see `CONTRIBUTING.md`) and list of what you're planning to test. Update this section with results as tests are completed.

- How was this PR tested? Examples include (but are not limited to):
    - Terraform developers should expect atlantis to successfully execute `atlantis plan`
    - Image development should expect to run a successful `packer build`
    - Lambda development should expect to publish lambdas with a successful `build awslambda`

> If a PR is to be promoted, the test section is **REQUIRED** to be filled in completely.

## Change Request

A Change Request must be filed and approved in Sparc for to apply changes to prod roots.
If there are prod changes in this pull request, please list their IDs here.

(If there are no prod changes in this PR, this section can be ignored or deleted.)

## Review
Reviewers should ensure that at least the following criteria have been met:

- [ ] Reviewer has read every line of the code being changed (i.e. in the "Files changed" tab on Github or with `git diff`)
- [ ] PR meets the described objectives
- [ ] PR does not contain extraneous changes that do not contribute to a described objective
- [ ] (For terraform changes) An atlantis plan has been run on the most recent version of code in the PR (i.e. after the last push)
- [ ] (For terraform changes) Reviewer has read every line of the final atlantis plan
- [ ] Code in PR is of sufficient quality
- [ ] Commits in PR are meaningful (e.g. no "fix typo in my previous commit"-type messages)
