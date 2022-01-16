# Intro
This guide will help you create a multisig wallet with the following characteristics:
- Electrum as the software to create and coordinate.
- 2 of 3 signature scheme.
- One online laptop, i.e. connected to Internet.
- One airgapped ColdCard, i.e. not to be connected with a PC ever.
- One or two airgapped laptops, depending if you'll store your seeds in different geographical locations.
- No other parties involved, that is, this is a wallet we are configuring for ourselves.

While we are using a 2 of 3 set-up, the instructions here will serve to a more general multisig structure with as many cosigners as you wish.

Equally important is that I use one Coldcard here, but more are possible. The key is to know how to proceed with at least one. After that, you can follow the same steps if you wish to add more ColdCards to your setup.

Also, if you want to configure your multisig *only* using airgapped ColdCards, then you can just follow the instructions already published by Coinkite here:  
https://www.youtube.com/watch?v=OMpZ5heLsRg

The reason to write this guide is that I didn't find immediately obvious how to create the setup described above. 
In particular, I followed intensively these two guides but in order to get things working, at some point during the process, I had to connect the ColdCard to my computer, which I wanted to avoid at all costs: 
- [How to store your bitcoin in Multisig, by Arman The Parman](https://armantheparman.com/how-to-store-your-bitcoin-detailed-instructions-part-2-multi-signature/)
- [Multisig documentation, by ColdCard](https://coldcard.com/docs/multisig)

My instructions draw a lot from those two, so if you don't mind to connect  a ColdCard via USB, I'd recommend you follow those guides directly, instead of this one.

Without further ado, let's start.

# Create three seeds
As you know by now, a mnemonic seed is a  human-readable representation of a private key. In our multisig set up, 2 of 3, we need to generate three seeds. In the future, we will only two of them to spend bitcoin from this wallet.

To achieve the generation in a secure way, there are many tutorials and methods. 
I particularly like the 'diceware' method developed by taelfrinn here:  
https://github.com/taelfrinn/Bip39-diceware

This is pretty much a mapping of all BIP39 seed words to a code that you can get using one coin and four dice.

Beware, to complete the previous, you also need to generate the checksum (that is the 12th or the 24th word, depending on how long your seed will be).

If you want to generate the checksum automatically, you can download this html code and run it in an airgapped computer:  
https://github.com/merland/seedpicker/tree/master/calculator 

Arman also provides two guides to generate your seed:  
- [Simple way](https://armantheparman.com/how-to-safely-generate-your-bitcoin-mnemonic-seed-phrases/)
- [Hard way](https://armantheparman.com/bitcoin-seed-with-dice/)

# Set up the airgapped laptop(s)
For this guide, I am assuming that we will have three signing devices distributed geographically. Therefore we will need to set up two airgapped laptops plus one ColdCard. Later on, we shall transport each device to the desired location.

In another very comprehensive guide, Arman explains [how to create an airgapped computer with a Raspberry Pi Zero](https://armantheparman.com/how-to-set-up-a-raspberry-pi-zero-air-gapped-with-electrum-desktop-wallet/). If this is your preferred solution, please follow that guide for the airgapping.

In my case, since I had a couple of old laptops I was not using any longer, I decided to repurpose them as airgapped signing devices.


[Linux Mint distribution](https://linuxmint.com/)  

You will have to install Electrum here from an online computer. Arman also describes that in this guide, but I will go ahead and summarize it here:
...
# Install Electrum in the airgapped laptop(s)

You will have to install Electrum here from an online computer. Arman also describes that in this guide, but I will go ahead and summarize it here:
...

# Set up the Multisig wallet (watch-only) from the online laptop
We need an online laptop for the following:
- Set up the wallet structure and export it to the other devices.
- Watch the movements of that wallet (check if transactions are going in and out).
- Create unsigned transactions everytime we want to spend our coins from the multisig wallet.




# Configuring the Multisig wallet in the ColdCard

There is an option to "trust public keys" in a msig tx

# Resources
This guide was only possible after reading the very useful materials by ColdCard and Arman The Parman here:  

https://armantheparman.com/how-to-store-your-bitcoin-detailed-instructions-part-2-multi-signature/  

https://coldcard.com/docs/multisig