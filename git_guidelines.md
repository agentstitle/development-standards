Git Guidelines and Best Practices
=================================

Date Created: 2018-05-30  
Last Modified: 2018-05-30    

## Summary

This document describes the conventions and best practices applicable to Agents Title project repositories.

Agents Title uses master or "trunk" development -- where the code for production is kept in the master branch and is pull request/merged to. The other branches are used for staging and development.

### Table of Contents

- [Git Branching](#git-branching)
- [Development Flow](#development-flow)

## Git branching

Source code is currently hosted on [Github](http://github.com/agentstitle/). The following branches are used in each project:

- dev-* (name for the feature and developer: `dev-kt-newdatabase`)
- stage
- master (or prod) <- has branch protection and requires PRs

## Development flow

1. Make all your changes in a dev branch.
2. Pull request (PR) into stage branch (do code review in PR) and perform end-to-end integration testing.
3. Pull request from dev into master, force a review and approvals before deployment.
4. **Squash-merge** into master with good release notes and new version.
5. Delete merged dev branch.
6. Delete stage branch. 
7. Create new stage branch from master.

**NOTE:** Always branch from the master branch for your new branches.
