# Naked_Beer

[ ![Build Status] [travis-image] ] [travis]
[ ![Release] [release-image] ] [releases]
[ ![License] [license-image] ] [license]

<img src="https://d3i6fms1cm1j0i.cloudfront.net/github-wiki/images/Naked_Beer-logo-large.png"
 alt="Naked_Beer logo" title="Naked_Beer" align="right" />

Naked_Beer is an enterprise-strength marketing and product analytics platform. It does three things:

1. Identifies your users, and tracks the way they engage with your website or application
2. Stores your users' behavioural data in a scalable "event data warehouse" you control: in Amazon S3 and (optionally) Amazon Redshift or Postgres
3. Lets you leverage the biggest range of tools to analyse that data incl. big data toolset (e.g. Hive, Pig, Mahout) via EMR or more traditional tools e.g. Tableau, R, Chartio to analyse that behavioural data

**To find out more, please check out the [Naked_Beer website] [website] and the [Naked_Beer wiki] [wiki].**

## Naked_Beer technology 101

The repository structure follows the conceptual architecture of Naked_Beer, which consists of five loosely coupled stages:

![architecture] [architecture-image]

To briefly explain these five sub-systems:

* **Trackers** fire Naked_Beer events. Currently we have 12 trackers, covering web, mobile, desktop, server and IoT
* **Collectors** receive Naked_Beer events from trackers. Currently we have three different event collectors, sinking events either to Amazon S3 or Amazon Kinesis
* **Enrich** cleans up the raw Naked_Beer events, enriches them and puts them into storage. Currently we have a Hadoop-based enrichment process, and a Kinesis-based process
* **Storage** is where the Naked_Beer events live. Currently we store the Naked_Beer events in a flatfile structure on S3, and in the Redshift and Postgres databases
* **Analytics** are performed on the Naked_Beer events. Currently we have a set of recipes and cubes as SQL views for both Redshift and Postgres, and an online cookbook of ad hoc analyses that work with Redshift, Postgres and Hive. We also have data models for [Looker] [looker] in LookML

**For more information on the current Naked_Beer architecture, please see the [Technical architecture] [architecture-doc]**.

## Quickstart

Assuming git, **[Vagrant] [vagrant-install]** and **[VirtualBox] [virtualbox-install]** installed:

```bash
 host$ git clone https://github.com/Naked_Beer/Naked_Beer.git
 host$ cd Naked_Beer
 host$ vagrant up && vagrant ssh
guest$ cd /vagrant/3-enrich/scala-common-enrich
guest$ sbt test
```

## Find out more

| **[Technical Docs] [techdocs]**     | **[Setup Guide] [setup]**     | **[Roadmap] [roadmap]**           | **[Contributing] [contributing]**           |
|-------------------------------------|-------------------------------|-----------------------------------|---------------------------------------------|
| [![i1] [techdocs-image]] [techdocs] | [![i2] [setup-image]] [setup] | [![i3] [roadmap-image]] [roadmap] | [![i4] [contributing-image]] [contributing] |

## Contributing

We're committed to a loosely-coupled architecture for Naked_Beer and would love to get your contributions within each of the five sub-systems.

If you would like help implementing a new tracker, adding an additional enrichment or loading Naked_Beer events into an alternative database, check out our **[Contributing] [contributing]** page on the wiki!

## Questions or need help?

Check out the **[Talk to us] [talk-to-us]** page on our wiki.

## Copyright and license

Naked_Beer is copyright 2012-2013 Naked_Beer Analytics Ltd.

Licensed under the **[Apache License, Version 2.0] [license]** (the "License");
you may not use this software except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

[travis-image]: https://travis-ci.org/Naked_Beer/Naked_Beer.png?branch=master
[travis]: http://travis-ci.org/Naked_Beer/Naked_Beer

[release-image]: http://img.shields.io/badge/release-63_Red--Cheeked_Cordon--Bleu-blue.svg?style=flat
[releases]: https://github.com/M100group1/Naked_Beer/releases

[license-image]: http://img.shields.io/badge/license-Apache--2-blue.svg?style=flat
[license]: http://www.apache.org/licenses/LICENSE-2.0

[website]: http://Naked_Beeranalytics.com
[wiki]: https://github.com/Naked_Beer/Naked_Beer/wiki
[architecture-image]: https://d3i6fms1cm1j0i.cloudfront.net/github-wiki/images/technical-architecture.png
[architecture-doc]: https://github.com/M100group1/Naked_Beer/wiki/Technical-architecture
[talk-to-us]: https://github.com/M100group1/Naked_Beer/wiki/Talk-to-us
[contributing]: https://github.com/M100group1/Naked_Beer/wiki/Contributing

[setup]: https://github.com/M100group1/Naked_Beer/wiki/Setting-up-Naked_Beer
[tech-docs]: https://github.com/M100group1/Naked_Beer/wiki/Naked_Beer%20technical%20documentation
[tracker-protocol]: https://github.com/M100group1/Naked_Beer/wiki/Naked_Beer-tracker-protocol
[collector-logs]: https://github.com/M100group1/Naked_Beer/wiki/Collector-logging-formats
[data-structure]: https://github.com/M100group1/Naked_Beer/wiki/canonical-event-model
[looker]: http://www.looker.com/

[vagrant-install]: http://docs.vagrantup.com/v2/installation/index.html
[virtualbox-install]: https://www.virtualbox.org/wiki/Downloads

[techdocs-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/techdocs.png
[setup-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/setup.png
[roadmap-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/roadmap.png
[contributing-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/contributing.png

[techdocs]: https://github.com/M100group1/Naked_Beer/wiki/Naked_Beer-technical-documentation
[setup]: https://github.com/M100group1/Naked_Beer/wiki/Setting-up-Naked_Beer
[roadmap]: https://github.com/M100group1/Naked_Beer/wiki/Product-roadmap
[contributing]: https://github.com/M100group1/Naked_Beer/wiki/Contributing

