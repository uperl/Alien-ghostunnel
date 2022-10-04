# Alien::ghostunnel ![static](https://github.com/uperl/Alien-ghostunnel/workflows/static/badge.svg) ![linux](https://github.com/uperl/Alien-ghostunnel/workflows/linux/badge.svg)

Find or install ghostunnel TLS proxy

# SYNOPSIS

```perl
use Alien::ghostunnel;
use Env qw( @PATH );

unshift @PATH, Alien::ghostunnel->bin_dir;

system 'ghostunnel', ...;
```

# DESCRIPTION

This [Alien](https://metacpan.org/pod/Alien) will find or build [ghostunnel](https://github.com/ghostunnel/ghostunnel),
and make it available to Perl modules.  Ghostunnel is a simple TLS proxy with mutual
authentication support for securing non-TLS backend applications.

If there is a known binary build on the `ghostunnel` project page for your platform,
then that will be downloaded.  Otherwise if you have a Go compiler available it will
be built from source.  If neither of those options work then you are out of luck,
unfortunately.

If for whatever reason you prefer not to install the binary version of ghostunnel,
you can set `ALIEN_GHOSTUNNEL_SOURCE` to a true value when installing:

```
$ env ALIEN_GHOSTUNNEL_SOURCE=1 cpanm Alien::ghostunnel
```

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2022 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
