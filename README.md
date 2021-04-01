# exportSwarmKey

`exportSwarmKey` is a command-line utility to get the Ethereum keys from your Swarm keystore file. 

We reccomend the usage of `bee-clef`, but if you inadvertedly started `bee` without `bee-clef`, this is as good as it gets.

## Once you have your key

- Make a backup of your key in a safe place
- Import your keys to a trusted Ethereum wallet (such as Metamask)
- Validate that the address inside your wallet corresponds with the Ethereum address of your Bee node (`curl localhost:1635/addresses`)

## Releases

You'll find pre-built releases of this tool under Releases in the top right corner of this page.  Using a release eliminates the need for having a go development environment.

Download the appropriate release for your platform and execute it with the following command:

`exportSwarmKey \<sourceDirContainingBeeKeys\> \<password\>`

## Buillding from Source

If you want to build the tool from source, the following information should help get you running.

### Requirements
- [golang](https://golang.org/doc/install)
- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### HowTo
- Clone this repo and navigate to directory
- run `go run main.go \<sourceDirContainingBeeKeys\> \<password\>`
- read "Once you have your key" above

With gratitude to @jmozah <3

## Warning
Never interact with your chequebook directly, but always do so via `bee` APIs. If you would call into functions of your chequebook with your imported key in Metamask, you might screw things up for Bee.
