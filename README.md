# illumos Closed Bits

There are, and always have been some closed bits as part of illumos. These bits
were originally obtained by multiple partiesfrom
http://dlc.sun.com/osol/on/downloads/current/ at the time that OpenSolaris was
opened . The parts of the closed bins that are used are a few various drivers
(e.g., mtp, bnx), the IPSEC IKE daemon, and pax(1). This came up on
[illumos-developer@][3] recently.

This repo is meant to be a record, and an independently verifiable source for
ensuring that they haven't changed.

This repo contains various hashes of closed tar files used during the SmartOS
build process. If the integrity of a source is in question, you may verify
them here.

There are known weaknesses in several hashing algorithms, but at current there
is no known weakness effective at producing collisions in multiple algorithms
simultaneously.

The hashes were generated from the tar files downloaded from the [SmartOS build
system locations][1] and have verified against independent copies used for
OmniOS and Nexenta. In order for there to be a compromise, all copies would
need to be simultanously compromised, or a sufficient conspiracy.

The following can be used for cross reference. The checksum of the files can
be verified against the [Hashes](./Hashes) file in this repository.

* Joyent [pub/build/illumos][5] dated 2010-08-18
* OmniOS [developer/illumos-closed][2] package dated 2016-11-01
* OmniTI [illumos-gate][4] mirror dated 2012-08-06

For further integrity verification, you can clone this repo to ensure that I
have not changed the hashes with a forced push.

[1]: https://github.com/joyent/smartos-live/blob/master/sample.configure.smartos#L27-L32
[2]: https://pkg.omniti.com/omnios/r151020/info/0/pkg%3A%2F%2Fomnios%2Fdeveloper%2Fillumos-closed%405.11%2C5.11-0.151020%3A20161101T224748Z
[3]: https://illumos.topicbox.com/groups/developer/T5cf348469c9ec7a3-M8baaf354c1f2d91acd8c23c4
[4]: https://mirrors.omniti.com/illumos-gate/
[5]: https://download.joyent.com/pub/build/illumos
