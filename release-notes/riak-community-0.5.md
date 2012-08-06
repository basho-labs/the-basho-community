# Release Notes - The Riak Community v0.5

The following release notes chronicle the key events that happened in the Riak Community from approximately July 1 thru August 1. If you have something contribute, please [submit a pull request](https://github.com/basho/the-riak-community/pulls). (We want everything the community has done, so don't hesitate to add something for a past set of release notes.)

Jump to:

* [Blog Posts and Podcasts](#blog-posts-and-podcasts) 
* [Documentation](#documenation)
* [Meetups](#meetups)
* [Talks, Slide Decks, and Other Preso](#talks-slide-decks-and-other-presos)
* [Other Awesome Things The Community Did](#other-awesome-things-the-community-did)
* [New Known Production Deployments](#new-known-production-deployments)

----

### Blog Posts and Podcasts 

* Russell Brown wrote [a blog post](http://basho.com/blog/technical/2012/07/02/folsom-backed-stats-riak-1-2/) about the new stats code that is shipping with Riak 1.2. [**July 2**]
* Mathias Meyer [wrote a blog post](http://www.paperplanes.de/2012/7/5/six-ish-months-of-ebook-sales-riak-handbook.html) about his experience selling the Riak Handbook. [**July 5**]
* Ray Jenkins wrote [a blog post](http://blog.boundary.com/2012/07/09/reusable-patterns-for-riak-in-scala/) discussing riak-scala-dao, a simple, reusable persistence layer for Riak, written in Scala. [**July 9**]
* The team at GoGrid [wrote a blog post](http://blog.gogrid.com/2012/07/09/create-a-basho-riak-cluster-on-gogrid/) explaining how to setup a Riak cluster on GoGrid. [**July 9**]
* Lei Gu [wrote a blog post](http://2rdscreenretargeting.blogspot.com/2012/07/why-we-chose-riak-as-persistence.html) about why he and his team are going with Riak. [**July 10**]
* OJ Reeves [released](http://buffered.io/posts/webmachine-erlydtl-and-riak-part-5/) the long-awaited fifth installment to his Riak, Webmachine, and Erly DTL blog series. [**July 10**]
* Lei Gu [wrote up some details](http://2rdscreenretargeting.blogspot.com/2012/07/riak-java-client-distilled.html) on working with the Riak Java Client.
* Scott Leberknight [wrote a brief introduction to Riak](http://cloud.dzone.com/articles/brief-introduction-riak) and the Ruby client. [**July 12**]
* DevOps Angle [posted a quick blog](http://devopsangle.com/2012/07/12/nosql-database-religion-comparing-riak-to-others/) about the Riak Comparisons on our wiki. [**July 12**]
* Shai Rosenfeld [wrote a blog post](http://shairosenfeld.com/blog/index.php/2012/07/riak-shim/) about the riak-shim code he, mkb, and EngineYard released. [**July 13** ]
* Sean Cribbs [put together some details](http://basho.com/blog/technical/2012/07/18/Protobuffs-in-Riak-1-2/) on what's coming to the Protocol Buffers interface in Riak 1.2.[**July 18**] 
* Charles Gildawie [released a post](http://nosqlsolution.blogspot.com/2012/07/fun-with-riak.html) about his first impressions of Riak. [**July 23**]
* Jeremy Ong [put together a post](http://www.jeremyong.com/blog/2012/07/23/secondary-indices-in-riak-with-erlang/) about working with Secondary Indices and the Erlang client. [**July 23**]
* James Governor of RedMonk [wrote a quick post](http://redmonk.com/jgovernor/2012/07/25/basho-comes-to-shoreditch-a-tech-city-and-redmonk-story/) about Basho's new office in London. [**July 25**]
* Rodrigo de Castro wrote three blog posts about Riak in July. The first was called [Understanding Vector Clocks](http://architects.dzone.com/articles/understanding-vector-clocks). [**July 25**]
* Rodrigo also [wrote up some details](http://architects.dzone.com/articles/how-use-precommit-hook-riak) about using Pre-commit Hooks. [**July 26**]
* Rodrigo's last post was [a high-level overview](http://architects.dzone.com/articles/why-i-think-riak-great-nosql) of why he likes Riak. [**July 30**]

### Documentation 

* We added a [Riak and Couchbase comparison](http://wiki.basho.com/Riak-Compared-to-Couchbase.html) to the Riak Wiki. [**July 10**]
* We added a [Riak and HBase comparison](http://wiki.basho.com/Riak-Compared-to-HBase.html). [**July 11**]
* We added a [Riak and CouchDB comparison](http://wiki.basho.com/Riak-Compared-to-CouchDB.html). [**July 12**]
* The [Client Libraries page](http://wiki.basho.com/Client-Libraries.html) got a nice face lift courtesy of Sean Cribbs. [**July 15**]
* A [Searching and Aggregating Data](http://wiki.basho.com/Searching-and-Aggregating-Data.html) section was added to the wiki. (**July 20**) 


### Meetups

* Artur Bergman of Fastly and Dave Dawson of MIG discussed performance in distributed systems at the [second London Riak Meetup](http://www.meetup.com/riak-london/events/69174012/). [**July 5**]
* Ben Mills discussed how Braintree uses Riak in production at Braintree at the [first Chicago Riak Meetup](http://www.meetup.com/Chicago-Riak-Meetup/events/70017472/). [**July 11**] 
* Tom Santero gave an overview of Riak, and Sean Cribbs delivered a Preview of Riak 1.2 at the [inaugural Philadelphia Riak Meetup](http://www.meetup.com/Philly-Riak-Meetup/events/67994362/). [**July 19**]
### Talks, Slide Decks, and Other Presos

* InfoQ released a [video](http://www.infoq.com/presentations/Knockbox-an-Eventual-Consistency-Toolkit) of Reid Draper's Knockbox talk from Clojure/West. [**July 10**]

### Code Releases 

* Shuhao Wu completely refactored and released a new version of [riakkit](https://github.com/ultimatebuster/riakkit), a Python Riak ORM. [**July 4**]
* The team at Trifork released the [beginnings of a C Client](https://github.com/trifork/riack) for Riak. [**July 5**]
* Ray Jenkins released [riak-scala-dao](https://github.com/rjenkins/riak-scala-dao), a reusable persistence layer for Riak written in Scala. [**July 9**]
* We [started work](https://bugs.launchpad.net/charms/+bug/1022591) on a Riak Charm for Juju. [**July 9**]
* mkb and the team at EngineYard released some code called [riak-shim](https://github.com/mkb/riak-shim) that reads config/database.yml and generates sensible bucket names. [**July 11**]
* Tom Arnfeld released the beginnings of a Riak ORM for the Fuel PHP Framework. [**July 16**]
* Andrew Nelson's Data-Riak Perl client for Riak [eclipsed version 1.0](http://search.cpan.org/~anelson/Data-Riak-1.1/). [**July 26**]

### Other Awesome Things The Community Did

* Sebastian Röbke [shared a pretty amazing photo](https://twitter.com/boosty/status/220997388754632704) of what they do at they do at the Xing.com offices. [**July 9**]
* GitHub [announced](http://peter.a16z.com/2012/07/09/software-eats-software-development/) a new round of funding. [**July 9**]
* Boundary [announced](http://boundary.com/about/press/boundary-nets-15m-to-accelerate-the-future-of-it-monitoring-and-management) a new round of funding. [**July 10**]
* We announced [RICON](http://basho.com/community/ricon2012/), a two day conference dedicated to Riak, developers, and the future of distributed systems in production. [**July 16**]
* The team at Kiip [announced](http://blog.kiip.me/post/27401788412/kiip-raises-a-series-b) that they raised a new round of funding. [**July 17**]
* We announced a [new round of funding](http://gigaom.com/cloud/nosql-startup-basho-raises-11-1m-and-storms-japan/). [**July 17**]
* Zencoder [announced](http://blog.zencoder.com/2012/07/26/brightcove-acquires-zencoder/) that it was acquired by Brightcove. [**July 26**] 
* Dietrich Featherston [tweeted a photo](https://twitter.com/d2fn/status/228556585713143808) showing off the OLAP language he and the Boundary team have built on top of kobayashi, their Riak-based storage system. [**July 27**]

### New Known Production Deployments 

* [EnStratus](http://basho.com/company/production-users/#user-enstratus)
* [LoveIt](http://basho.com/company/production-users/#user-loveit)
* [Payango](http://basho.com/company/production-users/#user-payango)
