# Blockstored Primer

A standalone OS-wide service managing, storing,
distributing and analyzing IPLD blocks.

> This is part of a vision that all parts of IPFS
will eventually become distinct services.
I.e.: the Bitswap daemon is positioned between
the LibP2P daemon and the Blockstore daemon.

Blockstored lays between *clients*, dealing with
blocks and *repositories*, stroring these blocks
and their metadata.

Many different kinds of repositories have already
been developed by the IPFS-project.

> A CAR file can be a repository. Not good to be
written, but well.

> Maybe, someday, with the hypothetical WebOS,
there will be some specialized partition format for
storing blocks, or even some specialized hardware.
Who knows?

Interoperability between clients and Blockstored
can be done first through a HTTP-API. That API will
probably be a subset of the existing IPFS API.

> How to establish origins and permissions over
a HTTP-API? (see below)

In the future there might possibly be a
shared-memory based API.

Blockstored keeps track which clients have produced
a block. These clients are then called *origins*.
The origins can also specify whose other clients
may access the block.

