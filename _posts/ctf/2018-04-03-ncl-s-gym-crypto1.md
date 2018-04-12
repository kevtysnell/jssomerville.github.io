---
title: Hackney CTF
heading: Crypto 1 (Easy)
subheading: Simple hexidecimal conversion
author: Jesse Somerville
banner-pic: ncl.jpg
categories: ctf
layout: post
---

This is the first of several cryptography challenges in the Gym for NCL Spring 2018.  It serves as a jumping off point for the rest of the challenges.  It is pretty easy if you have any experience with crypto CTFs before.

## Nan
`0x73636f7270696f6e`
Looking at the first 'cipher', I can immediately tell that it is encoded in hexidecimal because it is in the form '0x0000'. This means all we have to do is decode the hex into ASCII and we will probably have our plaintext.

There are several ways that we can go about decoding it. I will show two ways: using an online hex-to-ascii converter and also using xxd in a bash shell.

#### Using an online hex-to-ascii converter
One site that can do this conversion for us is [RapidTable's Hex to ASCII text converter](https://www.rapidtables.com/convert/number/hex-to-ascii.html). I am going to just copy and paste the hex into the converter and see what it gives me.

![RapidTables Hex to ASCII]({{ "/ctf-img/ncl-s-gym-crypto1/rapidTables.jpg" | relative_url }})

As you can see, it converted the hex to ASCII and gave us the solution in plaintext: scorpion.

#### Using a bash shell and xxd
xxd is a command line tool that 'creates a hex dump of a given file or standard input'. It can also, conveniently for us, take in a hexadecimal string and output its ASCII equivalent.

I am going to use the command `echo 73636f7270696f6e | xxd -r -p`. 
echo will send the argument given to it to stdout, in this case, it's the hex string. 
-r tells xxd to convert hex to ASCII. 
-p tells xxd to use a plain format.

![xxd]({{ "/ctf-img/ncl-s-gym-crypto1/xxd.jpg" | relative_url }})

As you can see, I get the same solution as I did with the online converter before.


## Kristy
`YXBvbG9naXpl`
The type of encoding for this one is not quite as obvious as the first one. Typically, when I see a string like the one for this challenge, my first instinct is that it is base64 encoded. Base64 encoding takes each ASCII character, converts it to their respective ASCII byte codes, then concatenates those binary codes together. After that, the string of binary that results from the concatenation is split up into groups of 6 bits (6 bits have a maximum of 26 = 64 different binary values). These groups are then converted into individual numbers from left to right, which are then converted into their corresponding Base64 character values.

In order to test the hypothesis that this is in fact a Base64 encoding, I will just try to convert it and see if I get something coherent. Just like with Nan, I will show how to do it with both the online converter and with a bash shell.

#### Using an online base64 decoder
RapidTables also has a Base64 decoding app on their site. I am going to copy and paste the string that we have and see if it will decode it.

![RapidTables base64]({{ "/ctf-img/ncl-s-gym-crypto1/rapidTablesBase64.jpg" | relative_url }})


Perfect! It gave us apologize which is probably our solution.

#### Using a bash shell to decode the string
Bash has a built in function for encoding and decoding Base64 strings. It is simply called base64. In order to get it to do what we need it to do, we need to use the command echo YXBvbG9naXpl | base64 --decode. This command is pretty self explanatory, so lets just see it in action.

![base64]({{ "/ctf-img/ncl-s-gym-crypto1/base64.jpg" | relative_url }})

Nice, now we have gotten our solution using both methods.


## Stevie and Cassie
`01110011 01100101 01100101 01101101 01101001 01101110 01100111 01101100 01111001`
`01100010 01000111 00111001 01110011 01100010 01000111 01101100 01110111 01100010 00110011 01000001 00111101`
Both Stevie and Cassie have the same solution, so I will show how to do both of them by demonstrating with Stevie.

These are very obviously binary strings. All we have to do is convert them to ASCII. Once again, I will show how to do this using RapidTables and the bash shell.

#### Using an online binary-to-ASCII converter
Back on RapidTables, I'm going to go to the page for binary-to-ASCII conversion. I'm going to paste the binary string, convert it, and that will be our solution

![rapidTables binary]({{ "/ctf-img/ncl-s-gym-crypto1/rapidTablesBinary.jpg" | relative_url }})

And here you can see that our solution to Stevie is seemingly. Now you can do the same for Cassie.

#### Using bc to convert bases in bash
Here we are going to use a command line tool that serves as a binary calculator called bc. To convert the binary string to ASCII we will use the following command:
echo "obase=16; ibase=2; [binary string]" | bc | xxd -r -p

obase=16 means we want our output to be in base16
ibase=2 means that our input is a base2 number
And [binary string] is where the binary we want to convert would go

So this command is sending the hex conversion of the binary string to xxd which will convert it to ASCII.

![binary]({{ "/ctf-img/ncl-s-gym-crypto1/binary.jpg" | relative_url }})

Ta-da! We have our solution again


