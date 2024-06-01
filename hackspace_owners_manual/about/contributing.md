# What you need to know about making contributions

Contributions from anyone and everyone are very welcome! The aim of this manual
is to assist in the building of community and nothing says that better than
this being an open project.

## Licence

All content within this manual and associated documentation is licenced under
the [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported
license](https://creativecommons.org/licenses/by-nc-sa/3.0/).

# Making a contribution

The content in this manual is maintained via a Git repository on Github. What
that means is that we make use of the git version control system (VCS) to
manage how we create content. Whilst this may initially seem like a steep
learning curve, there are a number of ways in which you may contribute each
more technical than the last :)

## Finding the original

The Hackspace Owners Manual can be found on Github at
https://github.com/UKHackspaceFoundation/resources/tree/master/Hackspace%20Owners%20Manual

It's worth understanding that we have at least two "branches" of this at any given time.

The first branch is "master", this represents the current released version of the manual.

The second branch is "develop", this represents the current latest changes that
may or may not have been released yet.

Confused? Don't worry, we will endeavour to provide a mechanism for everyone to
contribute regardless how technical they are!

## Suggest a change

Email your correction(s) to ownersmanual@hackspace.org.uk and we'll fix it for
you!

If you're registered for the [Hackspace Foundation
Forum](https://forum.hackspace.org.uk/) then you can post a new topic there and
request your change. Someone from the team will try to pick up your request and
make your change for you.

If you have a github account and you've spotted an error, small correction, or
perhaps you'd like to see a new section in the manual you should create an
issue at https://github.com/UKHackspaceFoundation/resources/issues

## Copy the file and update it

If you have more changes than you can fit into an email asking for update, then
take a copy of the original file from above and make the corrections. Once
you've done that, drop us an email to ownersmanual@hackspace.org.uk telling us
which section of the manual this is for and include a copy of the file in your
email. Please remember to include a short summary of your change.

## Adding a new section

If you spot an area that you have experience with and want to contribute a
whole section we would be delighted. Drop us an email with your file and
suggest where you think it should live in the manual. Again please remember to
include a short summary of your change.

## Fork the git repository and submit a pull request

For the more technical members of the community, this section is for you. If
you are reading this section then it is assumed that you have a basic
familiarity with git and just need pointers into how we'd like you to
contribute.

Contributions should developed within a branch and submitted as pull requests.
In order to do this, you will need to follow a few steps.

* Fork the git repository

Visit https://github.com/UKHackspaceFoundation/resources and select 'Fork' in the top right of the page. You will be asked where you'd like to fork the repository to, choose your own account.

* Clone the new repository

In your newly created clone repository you will see a dropdown for 'Clone or
download'. Drop this down and select the mechanism you usually use to clone
(ssh is usual for Linux users), copy the text. Use this text to clone the repository. Assuming use of the command line client, this would look like this:
```
git clone git@github.com:idnorton/resources.git
```

You would expect idnorton to be replaced by your own github username.

* Create a feature branch

Once you have a clone of your repository, you should create a feature branch.
For the command line client this might look like this:
```
git checkout -b feature/my-feature-request
```

Where my-feature-request is replaced by a suitable feature request text.

* Make your changes

Follow the usual process of git add, commit and push to get your required
changes up to your github repository. If you're not sure how to do this then
feel free to ask for assistance on [the
forum](https://forum.hackspace.org.uk/).

Please remember to use sensible commit messages, if you need assistance on how
those might look then we recommend [How to write a commit
message](https://chris.beams.io/posts/git-commit/)

* Create a pull request

Once you've made your changes, committed them and pushed them up to your forked repository it's time to create the pull request. In your own fork, click on the button labelled 'New pull request'. This will take you to a new view, check that the following are correct:
```
base fork: UKHackspaceFoundation/resources
base: develop
```
In head fork should be your own repository followed by your branch.

You should be able to see all of your changes, carefully review these to make
sure that only the things you expect to have changed have changed. Next click
on the 'Create pull request' button and enter a suitable subject line and
description. When you are ready and happy with your subject line and
description click on the 'Create pull request' button.

Now you'll have to wait until someone is able to review your request and merge
it in for you. We'll do that as quickly as we can for you :) If you've seen no
reply and it's been a week since you submitted your Pull Request, please feel
free to post on the forum asking for someone to find time to review it.

We don't intentionally ignore people and we love it when people contribute
help, but we all have day jobs and sometimes might not have enough energy to
reply to you as quickly as we would like. We appreciate your efforts.

# Release the Manual!

This section is aimed at the technical team managing contributions and releases
of the manual. You'll need to have a github account and the required access to
be able to perform the actions described below.

The tecnical team need docs just like everyone else!

## Git Flow

We're using gitflow. There's a Debian package to assist with this under Linux:
```
apt-get install git-flow
```

Following your first checkout of the repo, initialise the git flow:

```
git clone git@github.com:UKHackspaceFoundation/resources.git
git flow init

iann@iann-desktop resources $ git flow init

Which branch should be used for bringing forth production releases?
   - develop
Branch name for production releases: [] master

Which branch should be used for integration of the "next release"?
   - develop
Branch name for "next release" development: [develop] 

How to name your supporting branch prefixes?
Feature branches? [feature/] 
Release branches? [release/] 
Hotfix branches? [hotfix/] 
Support branches? [support/] 
Version tag prefix? [] 
```

Once the git flow has been initialised, we can create a release. First let's look at the version number we're on:
```
iann@iann-desktop resources $ git describe origin/master
0.1.0
```

Create the new release:
```
iann@iann-desktop resources $ git flow release start 0.2.0
iann@iann-desktop resources $ git flow release finish 0.2.0
```

When prompted, enter a suitable message in the release tag to summarise the
changes that are being added by this release.

Once the release process has been completed, push it upstream along with the tags:
```
git push origin master develop --tags
``` 
