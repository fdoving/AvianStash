## Testing needed before merge to master and release

Anyone can participate in this testing.

You can get binaries from [SIG-Github](https://github.com/Ravenqt-RVN-SIG/Ravencoin/releases)

_CHECKSUMS.asc signed with fdovs PGP Fingerprint: 87EE482FE0942D570EBCFD8B6EECA6DEF1CFFB33_

### The version [4.7.0test1](https://github.com/Ravenqt-RVN-SIG/Ravencoin/releases)binaries will not sync on mainnet, known issue. 
Start with the -testnet argument or with the testnet shortcut. Syncing will take a while.

### The version [4.7.0test2](https://github.com/Ravenqt-RVN-SIG/Ravencoin/releases)binaries will work for both mainnet and testnet. 
If you want testnet, start with the -testnet argument or with the testnet shortcut. Syncing will take a while.

### Testing and selecting feature to test
If the github-issue linked in the results column is closed, testing is not needed. The status field can also give a hint. (If updated.)

### Results
Once you have tested a feature, please post results and feedback in the github-issue linked in the results column.

### Questions
If you have any questions find us in #ravenqt-sig-working on [Discord](https://discord.gg/jn6uhur)


| PR#  | Description          | Tests                         |Results| Status        |
|------|----------------------|-------------------------------|-------|---------------|
|[890](https://github.com/RavenProject/Ravencoin/commit/e5c4e87e5e58a429de2e4443ca00d0a7848217b5)|Dockerfile for full node|Build image from the file and test-run. Make sure starts and works.|[982](https://github.com/RavenProject/Ravencoin/issues/982)||
|[894](https://github.com/RavenProject/Ravencoin/commit/daf21eab44c68e46251148ac117305b6022ade37)|Price preview header|Make sure it works. Switch to all the options.|[983](https://github.com/RavenProject/Ravencoin/issues/983)||
|[898](https://github.com/RavenProject/Ravencoin/commit/74e4b223c35c733ff08b6c766a9fd9561e90c1f7)|Spinboxes Create Assets|Verify this works in as many cases as possible, switch to and from the view and select different asset types|[984](https://github.com/RavenProject/Ravencoin/issues/984)||
|[901](https://github.com/RavenProject/Ravencoin/commit/0ab725d6903bba080ea4552ea9d7e3330aa67391)|Configurable IPFS-viewer|Verify this works. Set your own, restart, reset, restart, etc. Try to break it with broken urls?|[985](https://github.com/RavenProject/Ravencoin/issues/985)||
|[917](https://github.com/RavenProject/Ravencoin/commit/d36cb41f10289edea7011a72248ca1a2d29a5dbf)|Configurable out of the box browsers|Verify this works. Set your own, restart, reset, restart, etc. The browsers will not work on testnet transcations. Testing this is easier if mainnet works. Try to break it with broken urls?|[986](https://github.com/RavenProject/Ravencoin/issues/986)||
|[926](https://github.com/RavenProject/Ravencoin/commit/ddc821eec726eafc7ba444b177d0190d785a0925)|Enable High DPI Scaling|Does this create unwanted side effects? OSX? Windows? font-sizes high/low res? Does it fix [870](https://github.com/RavenProject/Ravencoin/issues/870) ? |[987](https://github.com/RavenProject/Ravencoin/issues/987)||
|[927](https://github.com/RavenProject/Ravencoin/commit/ce3a6ed4f395ac0c64204c6fab76bd7d274a2493)|Transfer asset and Send view|Check units and default values in the spinboxes. Click the arrows in spinboxes.|[988](https://github.com/RavenProject/Ravencoin/issues/988)||
|[939](https://github.com/RavenProject/Ravencoin/commit/932a983bf0d9ea14a104457431b7576dcb1dcc49)|Redesigned mnemonic dialog|Create new wallets with all the options the new design gives.|[989](https://github.com/RavenProject/Ravencoin/issues/989)||
|[955](https://github.com/RavenProject/Ravencoin/commit/a8be3193f470837fbcefe63e54f45200e922ca59)|aarch64-linux build|Test the aarc64-linux binaries. Make sure they work.|[995](https://github.com/RavenProject/Ravencoin/issues/995)||
|[873](https://github.com/RavenProject/Ravencoin/commit/a7e305b16b104401b6efb890450a878467bd4c94)|P2SH for Assets|Construct transactions. Details will be provided. If not updated find us in discord.|[990](https://github.com/RavenProject/Ravencoin/issues/990)||
|OSX|Build/binaries|Test OSX binaries on various versions of OSX. |[991](https://github.com/RavenProject/Ravencoin/issues/991)||
|OSX64|Build/binaries|Test OSX64 binaries.|[991](https://github.com/RavenProject/Ravencoin/issues/991)||
|WIN|Build/binaries|Test Windows binaries on various versions of Windows. |[992](https://github.com/RavenProject/Ravencoin/issues/992)||
|LIN|Build/binaries|Test Linux binaries on various versions of Linux. |[993](https://github.com/RavenProject/Ravencoin/issues/993)||
|ARM|Build/binaries|Test arm-linux-gnueabihf binaries.|[994](https://github.com/RavenProject/Ravencoin/issues/994)||
|AARCH64|Build/binaries|Test aarch64-linux binaries.|[985](https://github.com/RavenProject/Ravencoin/issues/985)|Related to PR#955|
