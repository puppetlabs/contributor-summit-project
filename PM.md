# Project Management in GitHub

This page gives you some pointers on using a GitHub repository for effective project
management using built-in GitHub features. Open the [Settings](../../settings) page
of your reposititory to check them out.


## GitHub Wikis
You might choose to keep your project documentation in a Wiki to enable low-friction
collaborative editing. If you're creating a Puppet Module, you should use the
standard `README.md` and `REFERENCE.md` [documentation pattern](https://puppet.com/docs/puppet/latest/modules_documentation.html) to document your module.

Reference the [GitHub documentation](https://help.github.com/articles/about-github-wikis)
if you'd like more information.


## GitHub Projects
Project boards help you organize and prioritize your work. They are made up of issues,
pull requests, and notes organized as cards in columns. You can drag and drop the
cards and columns as needed. Get started by enabling the feature, then creating a new
board. Starting from a basic Kanban template will likely be the easiest way to get started.

Reference the [GitHub documentation](https://help.github.com/articles/about-project-boards)
if you'd like more information.


## Using this repository as a template:
This repository is set up with a project board and some starter issues to help keep you
on track. Using it is entirely optional, but some participants have found it helpful.
If you'd like to use it, just clone the repo and run the setup script.

1. Start off by creating a free GitHub account, if you don't already have one.
    * https://github.com/join
1. Fork this repository to your own namespace by clicking the *Fork* button in
   the top right of this page.
    * Remember to fork to your own namespace if you're a member of one or more organizations.
1. Now `clone` the repository to your own workstation.
    * Open your terminal window and navigate to the directory where you'd like to keep
      the local copy of your repository.
    * Run the command `git clone https://github.com/<your username>/contributor-summit-project`
1. Run the setup script to populate issues and milestones.
   1. Install a Ruby runtime if needed.
      * Windows: https://rubyinstaller.org
      * Linux: use your distributions package manager to install `ruby`.
   1. Run the command `./setup.rb`
 

# Questions?

* If I use the project template, can I change the name of my repository?
   * After the fork & clone are complete, you may change the name of the repository to
     match your project name better if you'd like.
* Why does the setup script ask for my GitHub credentials?
   * The script uses your credentials to configure your fork of the project repository.
     If you're using two-factor authentication, it will request a 2fa code and use that
     to create a temporary personal access token that's deleted at the end of the script.
   * The script is very short and clear. Please audit it to ensure no funny business.
   * If you're still not comfortable with this, then see the next question.
* What if I can't run the setup script?
   * The script just turns on the Issues queue and duplicates the milestones and issues from
     the template repository. You can do that manually if needed.
* What if I have other questions?
   * Email community@puppet.com and we'll do our best to answer it!

