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

## Note on CPAN ecosystem

Because the CPAN ecosystem only checked on author and module name and
version, and **not** on the `:auth` of the module, it has happened that
authors uploaded modules with an `:auth` different from the expected
`:auth<cpan:AUTHOR>` identity.  This has been corrected in this archive.

## Updating

This repository is expected to be updated using the
[Ecosystem::Archive::Update](https://github.com/lizmat/Ecosystem-Archive-Update) module.

## Directory structure

````
META.json
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
  |- ...
meta
  |- ...
  |- M
     |- ...
     |- Module::Name
         |- Module::Name:ver<0.0.1>:auth:<github:baz>:api<1>.json
         |- Module::Name:ver<0.0.2>:auth:<github:baz>:api<1>.json
         |- ...
     |- ...
  |- ...
sbom
  |- ...
  |- M
     |- ...
     |- Module::Name
         |- ...
         |- Module::Name:ver<0.0.1>:auth<foo:BAR>:api<1>.tar.gz.cdx.json
         |- Module::Name:ver<0.0.2>:auth<foo:BAR>:api<1>.tar.gz.cdx.json
         |- Module::Name:ver<0.0.3>:auth<zef:bar>:api<1>.tar.gz.cdx.json
         |- ...
     |- ...
  |- ...
````
