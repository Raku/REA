# Raku Programming Language Ecosystem Archive

The Raku Programming Language Ecosystem Archive (REA for short) attempts
to keep a copy of any distribution that has ever been released into the
Raku ecosystem.

## Synopsis

Because you may (and should) specify your module dependencies **with**
version (and possibly with authority and api version), you are guaranteed
that an application will continue to run, even though its dependencies
may have gotten updated (with a higher version number, or with a different
authority).

This however opens up a possible problem when trying to install an
application from scratch, and a particular version of a dependency is
no longer available in the "live" ecosystem.  In such a case, one
should be able to download and install the dependency from this
repository, or from any server front-end to this repository.

## Updating

This repository is expected to be updated using the
[Ecosystem::Archive](https://github.com/lizmat/Ecosystem-Archive) module.

## Directory structure

````
archive
  |- ...
  |- M
     |- ...
     |- Module::Name
         |- ...
         |- Module::Name:ver<0.0.1>:auth<foo:BAR>:api<1>.tar.gz
         |- Module::Name:ver<0.0.2>:auth<foo:BAR>:api<1>.tar.gz
         |- Module::Name:ver<0.0.3>:auth<zef:bar>:api<1>.tar.gz
         |- ...
     |- ...
git-meta
  |- ...
  |- Module::Name
      |- Module::Name:ver<0.0.1>:auth:<github:baz>:api<1>.json
      |- Module::Name:ver<0.0.2>:auth:<github:baz>:api<1>.json
      |- ...
  |- ...
cpan-meta
  |- ...
  |- BAR
      |- BAR:Module-name-0.0.1.json
      |- BAR:Module-name-0.0.2.json
      |- ...
  |- ...
````
