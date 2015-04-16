# Naked_Beer

[ ![Build Status] [travis-image] ] [travis]
[ ![Release] [release-image] ] [releases]
[ ![License] [license-image] ] [license]

<img src="https://github.com/M100group1/NakedBeer/images/Main_logo.png"
 alt="Naked_Beer logo" title="Naked_Beer" align="right" />

Naked_Beer is an web-based enterprise-strength marketing scheme with the following competences:
1. 	support, consultancy
2. 	business model innovation?
3. 	Brand recognition – brewers ore likely to sign up given expertise but wont be used to market to customers.


**To find out more, please check out the [Naked_Beer website] [website] and the [Naked_Beer wiki] [wiki].**

## Naked_Beer Concept

The repository structure follows the concepts of Naked_Beer, which consists of five loosely coupled stages:

![Market Research] [marketresearch-image]

To briefly explain these five sub-systems:

* **Extreme Users** 
-What can the design bring?
-What are the opportunities offered by Unibrew global challenges
-Energy recycling
-Process control

* **Industry Research and Business Model** 
(a) protection
(b) value chain
(c) entrepreneurial strategy
(d) business model

* **Environmental and Social aspects** 

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

[website]: https://github.com/M100group1/NakedBeer.git
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

