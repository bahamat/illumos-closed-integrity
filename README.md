# illumos Closed Bits

There are, and always have been some closed bits as part of illumos. These bits
were originally obtained by multiple parties from
<http://dlc.sun.com/osol/on/downloads/current/> during the time that OpenSolaris
was open. The parts of the closed bins that are used are a few various drivers
(e.g., mtp, bnx), the IPSEC IKE daemon, and pax(1). This came up on
[illumos-developer@][3] recently.

This repo is meant to be a record, and an independently verifiable source for
ensuring that they haven't changed. You can fork this repo

This repo contains various hashes of closed tar files used during the SmartOS
build process. If the integrity of a source is in question, you may verify
them here.

There are known weaknesses in several hashing algorithms, but at current there
is no known weakness effective at producing collisions in multiple algorithms
simultaneously.

The hashes were generated from the tar files downloaded from the [SmartOS build
system locations][1] and have verified against independent copies used for
OmniOS and Nexenta. In order for these files to be a compromised by a malicious
actor, all copies would need to be simultanously compromised, or a sufficient
conspiracy.

The following can be used for cross reference. The checksum of the files can
be verified against the [Hashes](./Hashes) file in this repository.

The official location for obtaining these objects is
<https://github.com/illumos/closed>. There are also the following independent
mirrors maintained by various illumos distributions.

* Triton [pub/build/illumos][5] mirror dated 2010-08-18
* OpenIndiana [osol/on/downloads][6] mirror dated 2010-08-18
* Tribblix [closed][7] mirror dated 2010-08-18
* OmniOS [developer/illumos-closed][2] package dated 2016-11-01

For further integrity verification, you can clone this repo to ensure that I
have not changed the hashes with a forced push.

[1]: https://github.com/TritonDataCenter/smartos-live/blob/master/sample.configure.smartos#L27-L32
[2]: https://pkg.omniti.com/omnios/r151020/info/0/pkg%3A%2F%2Fomnios%2Fdeveloper%2Fillumos-closed%405.11%2C5.11-0.151020%3A20161101T224748Z
[3]: https://illumos.topicbox.com/groups/developer/T5cf348469c9ec7a3-M8baaf354c1f2d91acd8c23c4

[5]: https://download.TritonDataCenter.com/pub/build/illumos
[6]: https://dlc.openindiana.org/dlc.sun.com/osol/on/downloads/20100817/
[7]: https://pkgs.tribblix.org/closed/