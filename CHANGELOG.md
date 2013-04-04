* 0.2.4 April 4, 2013
  * Fixed situations where client bootstrap fails due to a bad recipe, and the
    run_list isn't preserved, which meant to do further converges you would
    need to edit the node manually.
* 0.2.3 March 30, 2013
  * fix a bug where the automated security group generator would never actually find a collision
* 0.2.2 March 12, 2013
  * Vagrant box customizations via "customizations" attribute in
    `configure_vagrant`. Takes an array of arrays that are injected into the
    Vagrantfile as `vm.customize` lines. Patch by Greg Thornton.
  * Fixes around Net::SSH use of sudo and PTYs.
  * Some additional information about configuration in `chef-workflow-bootstrap`.
* 0.2.1 February 20, 2013
  * Fixate JSON dependnecy to keep knife from breaking in bundles.
* 0.2.0 February 8, 2013 
  * Several missing validation checks and edge races were resolved.
  * Significant internals refactor -- things that were fast and simple when
    things were small got less fast and simple later.
    * Ruby's singleton library used instead of ugly hax
    * Replace marshal system with a tie-alike database layer built atop sqlite
    * Everything is namespaced under ChefWorkflow::
    * Most of the things that break API above were marked deprecated and will print warnings if used.
  * Provisioners now have a 'report' method which is used in informational
    tasks to describe the provisioner's unique data.
  * Fix for knife bootstrap actually DTRT in chef 10.18.x
  * SSHHelper from testlib was moved here, now that it's used by tasklib as well.
  * Docs. Lots and Lots and Lots of Docs.

* 0.1.1 December 21, 2012
  * Fix gemspec. Here's to touching the stove.

* 0.1.0 December 21, 2012
  * Initial public release
