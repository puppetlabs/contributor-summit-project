# Contributor Summit Project Template

Contributor Summit project month is an experimental new format that builds on hack
sessions from past Contributor Summits and refocuses on long-term sustainability.
We're hoping that not only do you get a supported chance to play with some of our
new technology, but you can build it into something that contributes to the larger
DevOps community. We'll kick things off at Puppetize Live and make our first
releases at Contributor Summit Online, so this is a month-long collaborative hackathon!

We'll work with you throughout the month to help you maximine the value of your time
and reduce the amount of overhead you'll have to handle. See below for some of the
ways that Puppet can collaborate with you.

There are no real restrictions on what projects you can choose, only two suggestions:

1. You should be able to complete an [MVP](https://en.wikipedia.org/wiki/Minimum_viable_product) release in one month.
1. The project should contribute something positive to the world of DevOps.

This means that your project could be anything from a Puppet module, to a CI or
testing framework, to enhanced documentation for another project, to a process or
pattern proposal. The possibilities are endless!

We're glad that you're joining us on this adventure. It will be fun!

# Getting Started
It's easy to get going. We'll ask that you follow these steps and work from this
repository because it will make it much easier for us to keep track of who's working
on what projects and what your status is.

[GitHub has a useful tutorial](https://help.github.com/articles/fork-a-repo/) if you
need help with any of these steps.

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
 1. Tell us about your project:
      1. You'll need to create your [project charter](../../issues/1) first
      1. [Submit your project](https://goo.gl/forms/1g0znAZTyECzXD3q2)

## Using GitHub features
GitHub includes some optional repository features that you might be interested in.
Open the [Options](../../settings) page to check them out.

### GitHub Wikis
You might choose to keep your project documentation in a Wiki to enable low-friction
collaborative editing. If you're creating a Puppet Module, you should use the
standard `README.md` and `REFERENCE.md` [documentation pattern](https://puppet.com/docs/puppet/latest/modules_documentation.html) instead.

Reference the [GitHub documentation](https://help.github.com/articles/about-github-wikis)
if you'd like more information.

### GitHub Projects
Project boards help you organize and prioritize your work. They are made up of issues,
pull requests, and notes organized as cards in columns. You can drag and drop the
cards and columns as needed. Get started by enabling the feature, then creating a new
board. Starting from a basic Kanban template will likely be the easiest way to get started.

Reference the [GitHub documentation](https://help.github.com/articles/about-project-boards)
if you'd like more information.

# Collaboration Resources Provided
We would like to help ensure your success. We'll be working with you to help keep your
projects on track. We'll help you define your project scope and set roadmap goals, then
check in with you roughly weekly. (Milestones are scheduled for each Wednesday, but the
actual checkin date & time will vary.) In addition, during the project month we'll provide
several resources and services that you might not otherwise have access to.

Some of the resources will be provided via webinars or by downloaded materials and some
will be provided as short one-on-one chats or video consulations. The Puppet community
team will coordinate with each of you to ensure that you receive all the help you need.

See [the resources list](../../blob/master/RESOURCES.md) to see examples of what we could offer.

# Project Ideas
If you need a little inspiration to come up with a project idea, we've put together a 
[list of some suggestions](../../blob/master/PROJECTS.md). Feel free to use what you'd like from here,
no credit is needed.

If you'd like to collaborate with others for your project, please put a prominent note in
your project's `README.md` and socialize your idea in the `#contributor-summit` Slack
channel. And conversely, if you're looking to join a project, browse the [forks](../../network/members)
and see if any look exciting.

# Questions?

* Can I work on an existing project?
   * Sure! It would help us keep track of projects if you forked this repository and
     add your charter and a link to the actual project repository as the `README.md`
* Can I work on something that's not software?
   * Absolutely. Use this month to write a DevOps book, if you'd like! As you're defining
     your roadmap, you'll want to massage the issue queue to be more useful for the kind
     of project you want to work on.
* How will we communicate during the project month?
   * Project coordinators will contact you via email or Slack.
   * The [Puppet Community Slack](http://slack.puppet.com) has a #contributor-summit channel for conversation.
   * Email community@puppet.com if you need anything.
* Does this work count towards [Hacktoberfest](https://hacktoberfest.digitalocean.com)?
   * Most certainly! As long as the projects you're contributing to are public projects on
     GitHub, then any pull requests you make in the month of October will count towards
     the challenge.
* Can I change the name of my repository?
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

