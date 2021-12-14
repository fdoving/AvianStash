# AvianStash
Stash for Avian-stuff.

## bfg-fdov.sh
Quick hack to install depends, checkout a branch and build Avian.

Can build linux, arm32v7, aarch64, windows and osx. (if you get the SDK and put it in /tmp/SDKs/ as the only tar.gz file)

The SDK needs to be extracted like this: https://github.com/bitcoin/bitcoin/tree/master/contrib/macdeploy
(or if this is updated, check out the older bitcoin branches, like 0.18 etc)
For Avian 3.1.0: `MacOSX10.11.sdk` is the correct one.

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

9. `root@docker# AvianStash/bfg-fdov.sh linux master 10` args: platform gitbranch makethreads

10. Results will appear in /root/releases if everything works.
  
11. Alaternative to 9: `root@docker# AvianStash/bfg-fdov.sh linux,arm32v7,aarch64,windows,osx master 10` args: platform1,platform2 gitbranch makethreads



