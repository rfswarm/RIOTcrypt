# RIOTcrypt

This git was created to support and promote the usage of strong cryptographic algorithms on RIOT OS.

## TweetNaCl: a crypto library in 100 tweets

TweetNaCl is the smallest readable implementation of the NaCl crypto library. The cryptographic primitives chosen for NaCl allow fast implementations on a large variety of architectures. TweetNaCl was designed for small code size and memory footprint and cannot provide optimal run-time performance but should be usable on low-power embedded devices.

**Building TweetNaCl on RIOT OS**

The TweetNaCl source code can be downloaded from the authors homepage http://tweetnacl.cr.yp.to or can be found within this git repository. The latest version of RIOT OS is located on github https://github.com/RIOT-OS/.

```
wget tweetnacl.ct.yp.to/20140427/tweetnacl.c
wget tweetnacl.ct.yp.to/20140427/tweetnacl.h
```

The Public-key based encryption methods of TweetNaCl require a strong random number generation function that IS NOT shipped with the source code. The quality of the generated random numbers of the target device MUST be verified (see FIPS 140.2 section of this document) at least on the first use to guarante a realiable strong Public-key based encryption.

The generic random number generation function that is included within the first version of this RIOTcrypt git repository are only verified to be running on the RIOT OS "native" building target.
