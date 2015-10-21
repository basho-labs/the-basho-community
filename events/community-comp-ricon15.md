# RICON 2015 Community Competition
We want to have a friendly, uplifting competition headed into RICON 2015 that improves our community. Whether you can [attend RICON](http://bit.ly/ricon15e) or will **participate remotely**, jump in and share with your community!

The complete event is outlined at: http://bit.ly/ricon15comp

This file covers specific questions judges will ask themselves as they compare entries for the Best Demo RICON 2015 award. **This is not a complete list**, but rather a guide to think through some of the important details.

# Judging 

Considerations for the Best Demo RICON 2015.

* **Completeness** - project checks off each of the points under *Objective* above

    * *Required*

        * Is data stored in a Basho product? 

        * Can I GET data from the Basho product? 

        * Is there an interface to see how the Basho product is used?

        * Is there a clear branching strategy with a deployable master?

    * *Best if*

        * Can I PUT new values into the demo? 

        * Can I DELETE existing data from the demo? 

        * Does it behave as documented during network partition? 

        * Is there reasonable code abstractions? 

        * Is there a reasonable level of security considerations taken?

* **Documentation** - README.md (feel free to copy) and details on how it works

    * *Required*

        * Is the code on a public GitHub repo?

        * There is a README.md at the root of the project

        * README.md explains how to run the demo locally

        * README.md includes authors and license, [simliar to this repo](https://github.com/basho/riak-nodejs-client#license-and-authors)

    * *Best if*

        * Includes network diagram, [like this example](https://github.com/basho-labs/riak-mesos#director)

        * Manages features through Issues 

        * The work was completed with empathy for new users

        * The work was completed with empathy for future maintainers 

* **Creativity** - Does it make us smile? That x-factor that you can’t put a number on

    * *Required*

        * Project has a name

    * *Best if*

        * The name makes us smile 

        * The demo is unique 

        * The demo is meaningful to new developers

If you build a creative project with well-written documentation and don’t have it completed, you still can win over someone who completes something that has an empty README. 