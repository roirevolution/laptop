[comment]: # (If this closes something, say it here. For example, "Closes #10")

[comment]: # (What's the purpose of this PR? Is there anything in particular you'd like reviewers to know?)

[comment]: # (How can reviewers verify that the PR accomplishes its objective, if necessary?)

## Checklist
- [ ] I've reviewed the entire diff
- [ ] all changes are essential to what we're trying to achieve
- [ ] relevant tests added
- [ ] all tests passing
- [ ] relevant metrics added
- [ ] I've set up a reminder to set up dashboards and alerts (as needed) in Datadog once metrics start recording data
- [ ] no style issues
- [ ] documentation added/updated as necessary (go [here](https://docs.google.com/document/d/1JbH1-_GTI8MbIO-_PqKzOC-CQDq-5nO9i3indW8R76s/edit#) for a starting point)
* If there are migrations
  - [ ] plain strings or raw SQL are used where possible, so that the migration will work regardless of code versions or the environment
  * If data is modified or deleted
    - [ ] permanent data modification and deletion will happen at least a week after we're sure these migrations didn't break anything
    - [ ] I've created the followup PR with the migration to modify or delete data. Here's the link: **FILL THIS IN**
    - [ ] I've set up a reminder to deploy the followup PR in at least one week
  - [ ] tested against a copy of the production database
    - [ ] schemas change correctly during migration
    - [ ] data changes correctly during migration
    - [ ] schemas change correctly during rollback
    - [ ] data changes correctly during rollback
  - [ ] automated tests pass when run on the post-migration database
