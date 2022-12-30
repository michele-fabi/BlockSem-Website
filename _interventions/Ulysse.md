---
title: Ethereum Proof-of-Stake Under Scrutiny 
date: 16-12-2022
presenter:
  name: "Ulysse Pavloff"
  url: "https://www.linkedin.com/in/ulysse-pavloff/"
  affiliation: "CEA"
  image: "/assets/images/uly.jpg"
abstract: | 
 Ethereum has undergone a recent change called the Merge, which made Ethereum a Proof-of-Stake
 blockchain shifting closer to BFT consensus. Ethereum, which wished to keep the best of the two
 protocols designs (BFT and Nakomoto-style), now has an involved consensus protocol as its core.
 The result is a blockchain being possibly produced in a tree-like form while participants try to
 finalize blocks. Several attacks jeopardizing liveness have been found in this new setting. The
 Ethereum community has responded by creating a patch. We discovered a new attack on the patched
 protocol. To support our analysis, we propose a new formalization of the properties of liveness and
 availability of the Ethereum blockchain, and we provide a pseudo-code. We believe this formalization
 to be helpful for other analyses as well. Our results yield that the Ethereum Proof-of-Stake has
 probabilistic liveness, influenced by the parameter describing the time frame allowed for validators
 to change their mind about the current main chain.
paper: "https://hal.archives-ouvertes.fr/hal-03821290/file/main.pdf"
---
