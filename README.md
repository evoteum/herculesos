[//]: # (STANDARD README)
[//]: # (https://github.com/RichardLitt/standard-readme)
[//]: # (----------------------------------------------)
[//]: # (Uncomment optional sections as required)
[//]: # (----------------------------------------------)

[//]: # (Title)
[//]: # (Match repository name)
[//]: # (REQUIRED)

# herculesos

[//]: # (Banner)
[//]: # (OPTIONAL)
[//]: # (Must not have its own title)
[//]: # (Must link to local image in current repository)


![](images/hercules.png)

> [!IMPORTANT]
> **Pre-pre-alpha**
>
> HerculesOS is currently in active design and initial prototyping. Some sections of this README describe intended
> behaviour before implementation.
> 
> HerculesOS is not production ready yet!


[//]: # (Badges)
[//]: # (OPTIONAL)
[//]: # (Must not have its own title)



[//]: # (Short description)
[//]: # (REQUIRED)
[//]: # (An overview of the intentions of this repo)
[//]: # (Must not have its own title)
[//]: # (Must be less than 120 characters)
[//]: # (Must match GitHub's description)

The tug that brings your Kubernetes ships home for decommissioning

[//]: # (Long Description)
[//]: # (OPTIONAL)
[//]: # (Must not have its own title)
[//]: # (A detailed description of the repo)

HerculesOS is an in-memory operating system that can be used to remotely wipe disks on a target computer. This is
particularly useful when you have many computers that you want to recommission or decommission. It can be configured 

## Table of Contents

[//]: # (REQUIRED)
[//]: # (Managed automatically)
[//]: # (Changes between the TABLE_OF_CONTENTS_START and TABLE_OF_CONTENTS_END markers will be overritten)

[//]: # (TOCGEN_TABLE_OF_CONTENTS_START)

- [Security](#security)
- [Install](#install)
- [Usage](#usage)
- [FAQ](#faq)
    - [Why is it called "HerculesOS"?](#why-is-it-called-herculesos)
    - [How big will it be?](#how-big-will-it-be)
- [Documentation](#documentation)
- [Repository Configuration](#repository-configuration)
- [Contributing](#contributing)
- [License](#license)
    - [Code](#code)
    - [Non-code content](#non-code-content)

[//]: # (TOCGEN_TABLE_OF_CONTENTS_END)

## Security
[//]: # (OPTIONAL)
[//]: # (May go here if it is important to highlight security concerns.)

HerculesOS only has a small codebase, so the attack surface is tiny. Nonetheless, it is not designed to be a
long-running operating system.

[//]: # (## Background)
[//]: # (OPTIONAL)
[//]: # (Explain the motivation and abstract dependencies for this repo)



## Install

[//]: # (Explain how to install the thing.)
[//]: # (OPTIONAL IF documentation repo)
[//]: # (ELSE REQUIRED)

HerculesOS is designed to be booted using PXE. It will also be made available as a live image for booting from USB or
CD. If you still have CD's that is.

## Usage
[//]: # (REQUIRED)
[//]: # (Explain what the thing does. Use screenshots and/or videos.)

You will be able to configure how aggressive HerculesOS is with the following power levels.

| Power Level    | Action                                                                                                                     |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Idle Steam     | Light, non-destructive. Dry-run only.                                                                                      |
| Harbour Steam  | Wipes ephemeral state only (tmpfs, logs, kubelet dirs). Non-destructive to user data.                                      |
| Working Steam  | Standard disk wipe for reprovisioning the node.                                                                            |
| Full Steam     | Secure disk wipe. single-pass zero overwrite. Suitable for most disposal needs.                                            |  
| Boiler Redline | Enhanced-security disk wipe, n-pass overwrite (default 3, configurable). Suitable for disposal after highly sensitive use. |  

As with all things in the Kubernetes world, you will be able to do this in YAML.

[//]: # (Extra sections)
[//]: # (OPTIONAL)
[//]: # (This should not be called "Extra Sections".)
[//]: # (This is a space for ≥0 sections to be included,)
[//]: # (each of which must have their own titles.)

## FAQ
### Why is it called "HerculesOS"?

[Hercules](https://tugs.fandom.com/wiki/Hercules) the strongest tug boat from the classic TV show,
[TUGS](https://en.wikipedia.org/wiki/Tugs_(TV_series)). He is given the most important and dangerous jobs in his fleet.

Similarly, decommissioning a server is an important and dangerous job, which is why
[Drydock](https://github.com/evoteum/drydock) uses HerculesOS for the task.

This is because we love,
- obscure pop culture references.
- furthering the maritime theme of Kubernetes.

### How big will it be?

As small as possible, because the smaller he is, the faster he gets running, does his job, and then gets out of the way.
We are currently targeting 20MB.

For perspective, Candy Crush is approximately [326.2MB](https://apps.apple.com/cd/app/candy-crush-saga/id553834731). Not
really a fair "like for like" comparison, but you get the point!

## Documentation

Further documentation is in the [`docs`](docs/) directory.

## Repository Configuration

> [!WARNING]
> This repo is controlled by OpenTofu in the [estate-repos](https://github.com/evoteum/estate-repos) repository.
>
> Manual configuration changes will be overwritten the next time OpenTofu runs.


[//]: # (## API)
[//]: # (OPTIONAL)
[//]: # (Describe exported functions and objects)



[//]: # (## Maintainers)
[//]: # (OPTIONAL)
[//]: # (List maintainers for this repository)
[//]: # (along with one way of contacting them - GitHub link or email.)



[//]: # (## Thanks)
[//]: # (OPTIONAL)
[//]: # (State anyone or anything that significantly)
[//]: # (helped with the development of this project)



## Contributing
[//]: # (REQUIRED)
If you need any help, please log an issue and one of our team will get back to you.

PRs are welcome.


## License
[//]: # (REQUIRED)

### Code

All source code in this repository is licenced under the [GNU Affero General Public License v3.0 (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.en.html). A
copy of this is provided in the [LICENSE](LICENSE).

### Non-code content

All non-code content in this repository, including but not limited to images, diagrams or prose documentation, is
licenced under the
[Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) licence.
