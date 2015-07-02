# Release Notes - The Riak Community v0.7

The following release notes chronicle the known key events that happened in the Riak Community from approximately May 2015 thru *$DATE*. If you have something contribute, [please submit a pull request](https://github.com/basho-labs/the-riak-community/pulls). (We want everything the community has done, so don't hesitate to add something for a past set of release notes.)

Jump to:

* [Blog Posts and Podcasts](#blog-posts-and-podcasts) 
* [Meetups](#meetups)
* [Talks, Slide Decks, and Other Preso](#talks-slide-decks-and-other-presos)
* [Other Awesome Things The Community Did](#other-awesome-things-the-community-did)
* [New Known Production Deployments](#new-known-production-deployments)

----

### Blog Posts and Podcasts 

* 5/3/15 - [Comparison of Orleans to riak_core](http://christophermeiklejohn.com/papers/2015/05/03/orleans.html) by Christopher Meiklejohn
* 5/12/15-5/19/15 Mark Allen wrote detailed blog posts on riak_core, starting with [the basis of handoff](http://basho.com/understanding-riak_core-handoff/) and ending with [writing handoff functionality](http://basho.com/understanding-riak_core-handoff/)


### Meetups

* 5/14/15 - [NYC Riak](http://www.meetup.com/NYC-Riak-Meetup/events/220588748/) discussing Bitly's real-time bidding infrastructure

### Talks, Slide Decks, and Other Presos

* **The Final Causal Frontier** - Sean Cribbs at CraftConf ([Slides](https://speakerdeck.com/seancribbs/the-final-causal-frontier) | [Video](http://www.ustream.tv/recorded/61448875))
* Coding with Riak - Matt Brender at Velocity Conf ([Slides](http://www.slideshare.net/BashoTechnologies/coding-with-riak-from-velocity-2015))
* 

### Other Awesome Things Riak Users Did

* @tpjg let us fork his work on a Go client! ([Original](https://github.com/tpjg/goriakpbc) | [New Maintained](https://github.com/basho-labs/goriakpbc))
* A lot of people jumped into updating the Ansible presence for Riak and a [dev-2.x branch](https://github.com/basho-labs/ansible-riak/tree/dev-2.x) is in development
* [Mark Steele](https://github.com/marksteele) has [a cool PR merged](https://github.com/cmeiklejohn/riak_pg/pull/6) by Christopher that leverages CRDTs inside riak_pg
* Customers at [OneTwoTrip](http://onetwotrip.com) created a [Riak plugin](https://github.com/bosun-monitor/bosun/blob/master/cmd/scollector/collectors/riak.go) for [Bosun](https://github.com/bosun-monitor/bosun) to monitor Riak. Thank you for sharing it!
* Customers at [Sqor](https://sqor.com/) open sourced [their backup scripts](https://github.com/sqor/riak-tools) for Riak running in AWS and it's awesome

### New Known Production Deployments 
