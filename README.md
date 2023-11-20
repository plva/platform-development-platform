# platform-development-platform
platform-development-platform (pdp) is a development platform for developing development platforms.

# Project status

This is currently a federation of related-repositories, with a focus on command-line development built on and using free, open-source tools. The only supported hardware platform is Mac OS.

This repo acts as version control for a high-level aggregation of related repos.

## Related repos
- [todo]

# Start developing
**`START_NOTE`** 

*DO NOT RUN THIS YOURSELF.*

This step includes the potential for arbitrary code execution and is therefore insecure and incredibly risky to run. You should not trust that it's safe to do so even if others trust it, and you should not run this yourself.

The correct way to set this up is to locally clone all relevant repos and data from external URLs, to audit all the code, and to change the bootstrap and setup scripts to. This invariably involves the need for an expert in the loop, and for a new developer to be "initiated" into bootstrapping their development environment. Typically in a larger organization this is done by using an internal mirror of external repos that has been vetted and security-verified; in smaller organizations security is typically through obscurity (which means there's no security).

**REMOVAL OF THIS WARNING IMPLIES MALICIOUS INTENT**
**`END_NOTE`**

```
mkdir ~/pdp-dev && cd ~/pdp-dev && curl https://github.com/plva/platform-development-platform/bootstrap.sh >> bootstrap.sh && chmod +x bootstrap.sh && ./bootstrap.sh
```

# Development process and philosophy
## Bootstrappability
All tools and dependencies to be used for pdp development (which means all tools and dependencies used for developing pdp itself) must be bootstrapped from a single script using an already available scripting language (bash). Further levels of dependency-mangement bootstrapping should set up the automated provisioning process for a new developer's development environment (platform). All configuration, customization, and changes must be captured in version controlled files and should be replicable on a new hardware platform with a single command (the bootstrap/setup script). Manual steps are allowed as necessary to grant access to system permissions, but must be encapsulated in a manual-setup workflow that keeps track of which manual steps have been completed.

## Programmatical replicability
pdp development techniques and workflows are not considered "released" unless they are encapsulated in a self-documentating and programmatically replicable workflow. If you are using a development technique or workflow to develop, that technique is considered released, even if you haven't officially "released" it yet (into a commit, production, into the pdp ecosystem, etc). This means that your own development process must deliberately include forethought and planning into how your process itself can be replicated, and may require you to avoid techniques that you don't yet know how to replicate.

Of course, creating the tool that allows replicability of your process will often require a bootstrapping step where you are using a non-replicable process (e.g. inputting code into a free-form text editor), and this is initially unavoidable. This process is considered a critical breaking-bug in "production" and has very high priority, but may be "released" into "production" along with a plan to follow-up and fix the process.
