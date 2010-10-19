About
=====

This fork of BGHUDAppKit is the "recommended" fork for use in RapidWeaver plugin development. The reason for this fork is simply to draw a line in the sand so all plugin developers wishing to make use of the framework are working from the same source revision.

Usage
=====

RapidWeaver does not bundle BGHUDAppKit within it's application bundle. Therefore, plugin developers need to make sure to follow the steps below so as to minimize the possibility of conflicts.

1. Download the provided BGHUDAppKit release. This is a pre-built version of the framework and IB plugin.

2. Add the framework to your project and make sure to weak-link against it. Test that this is in fact working! We've seen cases where Xcode produces hard-linked binaries even though weak-linking has been setup in the Xcode project UI.

3. Make sure to test for the presence of BGHUDAppKit in code before attempting to load it. The first plugin to make use of the framework is responsible for loading it. All subsequent plugins can use the version resident in memory.

For examples of how to conditionally load frameworks at runtime from within your plugin or any other RapidWeaver related development questions, come join us on the RapidWeaver Developer Mailing List.

Development
===========

If you have changes/fixes for the framework, please direct them to the mainline before submitting a pull request to this fork. We will consider patches on this fork if they make sense for plugin developers but only if the mainline isn't interested in integrating them first.

Please see "README.textile" for more information about the framework from the mainline devs.
