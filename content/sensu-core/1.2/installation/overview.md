---
title: "Installation Overview"
description: "The complete Sensu installation guide."
weight: 1
product: "Sensu Core"
version: "1.2"
next: ../installation-strategies
menu:
  sensu-core-1.2:
    parent: installation
---

## The complete installation guide

The purpose of this guide is to help provide new and experienced Sensu users
alike with a detailed guide for installing and configuring Sensu into a variety
of operating environments. By default, this guide will direct you to install and
configure Sensu Core or Sensu Enterprise in a standalone configuration.

If you are a new Sensu user &ndash; or if you have only ever used automation
tools like [Chef][2], [Puppet][3], or [Ansible][4] to install and configure
Sensu &ndash; working through this installation guide for the exercise alone is
_strongly recommended_. Sensu's [architecture][5] is one of its most compelling
features, so learning how Sensu's components work together will greatly improve
your ability to leverage Sensu's architecture to your advantage.

_**NOTE: manual installation is recommended for pre-production environments
only.** Please note that this guide is not intended to provide instructions for
deploying Sensu into "production" environments. Production deployment strategies
&ndash; including using automation tools like Chef, Puppet, or Ansible to
install and configure Sensu &ndash; will be discussed [at the conclusion of this
guide][6]._

### Selecting an installation strategy

By default, this installation guide will focus on the instructions for
configuring a [standalone][10] installation, however instructions **are
available** for other configurations including [distributed][11] and
[high-availability][12]. Please consult the [installation strategies reference
documentation][13] for more information

### Installation overview

What will be covered in this guide:

1. [How to install and configure Sensu's prerequisites](../installation-prerequisites)
  - [How to install and configure Redis](../install-redis)
  - [How to install and configure RabbitMQ](../install-rabbitmq)
2. [How to install and configure the Sensu server and API](../install-sensu-server-api) (Sensu Core or Sensu Enterprise)
3. [How to install and configure a Sensu Client](../install-sensu-client)
4. [How to install and configure a Sensu Dashboard](../install-a-dashboard) (Uchiwa or Sensu Enterprise Console)
5. [Next steps](../summary)
  - [Monitoring infrastructure and applications with Sensu](../summary/#instrumentation)
  - [Automating Sensu installation](../summary/#automation)
  - [Hardening Sensu](../summary/#hardening)
  - [Running Sensu at scale](../summary/#scaling-sensu)

Upon the completion of the first four (4) steps in this guide, you should have a
fully functional Sensu installation, with one or more Sensu clients reporting
[keepalives][7] (Sensu's built-in "heartbeat" mechanism) back to the Sensu
server, _and_ a web-based Sensu dashboard providing visibility into the health
of your infrastructure.

Once you have  a fully functional Sensu installation, you will be encouraged to
move on to the  [Getting Started Guide][8], which will introduce you to  Sensu's
four primary building blocks (Checks, Handlers, Filters, and Mutators). But
let's not get ahead of ourselves...

### Installation requirements

What will you need to install Sensu?

- Familiarity with a modern command-line interface & related tooling
- Compute resources (e.g. one or more virtual machines, or physical computers)
- 30-60 minutes (the amount of time it should take to complete this installation guide)
- **OPTIONAL:** A [Sensu Enterprise][9] subscription (for
  installing Sensu Enterprise).

Ready? Let's get started with selecting an installation strategy!

[1]:  ../../quick-start/the-five-minute-install
[2]:  https://chef.io
[3]:  https://puppetlabs.com
[4]:  https://www.ansible.com
[5]:  ../../overview/architecture
[6]:  ../summary
[7]:  ../../reference/clients/#client-keepalives
[8]:  ../../guides/overview
[9]:  https://sensuapp.org/enterprise
[10]: ../installation-strategies/#standalone
[11]: ../installation-strategies/#distributed
[12]: ../installation-strategies/#high-availability
[13]: ../installation-strategies
