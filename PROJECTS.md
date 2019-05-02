# Project Suggestions

These are intended to be more inspirational than prescriptive. If this list prompts
a different idea, that's even better than snagging one of these. But do feel free
to run with anything on this list. Before claiming one, you might consider asking
around in [#contributor-summit](http://puppetcommunity.slack.com/app_redirect?channel=contributor-summit)
to see if you can join forces with someone already working on it.

* Puppet 6 introduces [Deferred functions](https://puppet.com/docs/puppet/6.0/integrating_secrets_and_retrieving_agent-side_data.html),
  which are evaluated during catalog application time -- eg, agent-side functions.
  This provides functionality for all kinds of exciting things: secret management,
  data that must be looked up by the agent, registering with some service that responds
  with an authentication token, etc. What kind of exciting things could you think of?
    * Suggested functions:
        * Retrieve secrets from [AWS secret manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/manage_retrieve-secret.html)
        * Generic *output of a `curl` command* function
    * Resources:
        * Follow an example project at [puppet-vault-demo](https://github.com/puppetlabs/puppet-vault-demo)
        * [Read a talk](https://twitter.com/binford2k/status/1092806318501576706) describing the appropriate use cases
        * Chat with the Core Puppet team during their Office Hours

* Bolt recently added the functionality for dynamically generating the nodeset.
  This means that you can now choose targets for your task or plan based on logic
  evaluated at runtime. Do you want to run an action all all your EC2 nodes based
  on a certain tag and uptime? Do you want to write other logic to target certain
  k8s containers?
    * Resources:
        * See the [pre-docs](https://github.com/puppetlabs/bolt/blob/master/pre-docs/inventory_version2.md) in the Bolt repository
        * Chat with the Bolt team during their Office Hours

* Types and Providers have long been a dark art. Recently though, we've released
  [a new library to simplify the job](https://puppet.com/docs/puppet/6.0/create_types_and_providers_resource_api.html).
  If there's always been that job you knew was suited for a type and provider, but didn't
  have the time to learn how -- now's the time. Build a new T&P or port an existing
  defined type to the Resource API.
    * Resources:
        * See the [developer docs](https://puppet.com/docs/puppet/6.0/create_types_and_providers_resource_api.html)
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel
        
* With the most recent release of [Resource API Transports](https://github.com/puppetlabs/puppet-specifications/blob/master/language/resource-api/README.md#transport) you can leverage the same code with Bolt and Puppet to integrate APIs and devices that can't (or shouldn't) run an agent into your configuration management. Do you have one of those systems or APIs that always get in your way because they don't integrate into Puppet and Bolt? Get it fixed!
    * Resources:
        * See the [specs](https://github.com/puppetlabs/puppet-specifications/blob/master/language/resource-api/README.md#transport)
        * Simple [example module](https://github.com/da-ar/hue_rsapi/pull/2) <!-- needs to be updated to the full module once this PR lands -->
        * Complex [example module](https://github.com/puppetlabs/puppetlabs-panos)
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel

* Puppet Server now comes with a new [CA command line tool and gem](https://puppet.com/docs/puppetserver/6.0/release_notes.html).
  It's far more reliable and is fully API driven, which leads to all kinds of neat
  possibilities.
    * Suggested projects:
        * It might be nice to have an open source graphical/web certificate management interface.
        * Are there any APIs that you think should be added or improved?
        * Perhaps you could make it possible to store the CA on object storage and make
          the Puppet stack fully "cloud native" and stateless
    * Resources:
        * See the [API docs](https://puppet.com/docs/puppetserver/6.3/http_certificate.html)
        * Chat with the Puppet Core team during their Office Hours
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel

* Do you have a favorite open source project? How are its docs? What about that one
  project? You know, the one with the default `README.md` created by GitHub... Maybe
  your project for this month could be writing documentation and a user guide.
    * Resources:
        * See the [tutorial](https://github.com/puppetlabs/contributor-summit-project/wiki) on writing a great README
        * Chat with the Docs team during their Office Hours

* We've been making a lot of advances in the Puppet Developer Experience with the
  PDK, the VSCode extension, and other tools. We'd love your help in creating an
  even better experience.
    * Suggested projects:
        * Help update `puppet-strings` to match all the great new Puppet language features.
        * Add documentation generation to the PDK using `puppet-strings`.
        * Build basic acceptance test generators using the smoke tests in the `examples` directory.
    * Resources:
        * See the [`puppet-strings` docs](https://github.com/puppetlabs/puppet-strings)
        * See the [PDK `CONTRIBUTING.md`](https://github.com/puppetlabs/pdk/blob/master/CONTRIBUTING.md) guidelines
        * Chat with the PDE team during their Office Hours

* Creating a `Puppetfile` is sometimes a tedious exercise. It would be much better if
  dependencies were resolved for you automatically. For that matter, there are many
  places in the Puppet ecosystem which would benefit from a dependency resolver.
  Perhaps you could build this in such a way that r10k could use it, the PDK could
  use it, etc. Maybe you could even wire up [an external library](https://github.com/CocoaPods/Molinillo)
  to do the hard work for you.
    * Resources:
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel
        * Chat with the PDE team during their Office Hours

* One of our SREs is creating a pipeline to make it easier for community members
  build the Puppet stack. One of the goals of the project is to make it easier to
  get Puppet and Bolt running on your Raspberry Pi devices. Would you like to get
  involved? The repository is pretty sparse now, but he's working on some content
  and contribution guidelines.
    * Resources:
        * See [the repository](https://github.com/puppetlabs/community-enablement-pipeline)
        * Chat with Gene Liverman (genebean), on the project board or in [Slack](https://puppetcommunity.slack.com/team/U3DCRQQKA).
        * Collaborate during Community Pipeline Project Office Hours

* One thing that has historically made Hiera hard to use is that it's not always
  clear what information is possible to retrieve for any given nodes combination
  of facts. With the v5 redesign, it's now theoretically possible script a way for
  `puppet lookup` to retrieve all that information by retrieving class and parameter
  data from the information service and then resolve each value. No such tool exists
  yet... perhaps you could build it?
    * Resources:
        * See the [information service API docs](https://puppet.com/docs/puppetserver/latest/puppet-api/v3/environment_classes.html)
        * Chat with Henrik during his Advanced Language Office Hours

* PQL is awesome and powerful, and like many things powerful it can be difficult to use.
  It would be great to have a graphical PQL editor and/or explainer. You can see some neat
  examples of something similar at https://regexr.com or at http://buildregex.com.
    * Resources:
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel

* Port the `augeasproviders_core` library to the new Resource API to be used as
  an alternative base to build parsing providers.
    * Resources:
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel

* The Puppet Server stack has been containerized, which opens us up to all sorts of nifty
  ideas. Perhaps you could create an auto-provisioned demo/training environment using
  [Pupperware](https://github.com/puppetlabs/pupperware). What else can you imagine?
    * Resources:
        * See the [Pupperware docs](https://github.com/puppetlabs/pupperware)
        * Chat in the [#puppet-dev](http://puppetcommunity.slack.com/app_redirect?channel=puppet-dev) Slack channel


---------

None of these pique your interest? Check around in [Slack](http://puppetcommunity.slack.com/app_redirect?channel=contributor-summit)
to see if you can join an existing project.
