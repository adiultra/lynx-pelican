Title: Using Github Releases
Date: 2016-03-28 18:30
Category: git
Tags: git, github

# Releases

Releases are a feature of github that allow developers to ship binaries for download so that the users of the software don't have to compile the source code and the developers don't have to add binary files to their repos.

> ### Note
>
> In this article Release means a new version of software that is `Released` By the developer for users to install and use.

## Usage

It's pretty easy to use. You get a link in your git-hub repo's mainpage named as Releases. Here is a screen-shot.


- If you didn't have any releases :

![Releases button](http://i.imgur.com/1dHp9Ay.png)

- If you had releases :

![Releases after](http://i.imgur.com/4m457jX.png)

You can navigate to it and follow instructions and then create a new/first release.

### Some points to remember

- Try to publish the release as compressed files and/or standalone executables.

- Don't include unnecessary files such as cache and `.git` folder.

- Use Pre-release option if your release is unstable.

- Version your Release to track record for changes.

---

## Tutorial

This tutorial is meant for those who for some reason could not publish a release. It is a simple step to step guide to publish a release.

> ### Note
>
> I have used my [notex](https://github.com/adiultra/notex) repo for this tutorial.

#### Step 1 :

Enter the release option.

![this is for you sagar, don't use a repo for storing exe](http://i.imgur.com/Jfvmp7p.png)

#### Step 2 :

Choose/Click(Whatever the heck you can call it) `Create a New Release`.

![The great button](http://i.imgur.com/3cTBs8X.png)

#### Step 3 :

![Read Description Below](http://i.imgur.com/Rjl3JDo.png)

1. Write description
2. Upload files
3. Select If a Pre-release
4. Publish The Release

A filled Release Form looks like :

![this](http://i.imgur.com/s47VGzm.png)

### Viola. Enjoy. You Just published your first Release.

![Viola](http://i.imgur.com/7r77MiV.png)
