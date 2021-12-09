# AvianStash
Stash for Avian-stuff.

## bfg-fdov.sh
Quick hack to install depends, checkout a branch and build Avian.

Can build linux, arm32v7, windows and osx. (if you get the SDK and put it in /tmp/SDKs/ as the only tar.gz file)

The SDK needs to be extracted like this: https://github.com/bitcoin/bitcoin/tree/master/contrib/macdeploy
(or if this is updated, check out the older bitcoin branches, like 0.18 etc)

The name of the tar.gz does not matter, the name of the directory it extracts does.


It must be run in a docker or some other discardable environment.
Designed to run as root with access to everything.
No sanitychecks, you should read it and understand it before using it.

_HyperPeek: And just for reference -- the docker build should have at least 8 GB of memory (I used 4 RAM, 4 swap). With only 2 swap the VM crashed._


Example usage:

1. `$ docker run -it ubuntu:bionic bash`

2. `root@docker# apt update`

3. `root@docker# apt install -y git`

4. `root@docker# cd`

5. `root@docker# git clone https://github.com/fdoving/AvianStash`

6. This is where you edit `AvianStash/bfg-fdov.sh` to adjust to your needs.

7. `root@docker# mkdir -p /tmp/SDKs`

8. `scp you@fileserver:/your/osx-sdk.tar.gz /tmp/SDKs/`  only needed if you want to build for osx.

10. `root@docker# AvianStash/bfg-fdov.sh linux master 10` <platform> <gitbranch> <makethreads>

11. Results will appear in /root/releases if everything works.



