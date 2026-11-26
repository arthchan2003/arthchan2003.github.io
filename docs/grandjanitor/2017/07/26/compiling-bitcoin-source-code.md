---
title: "Compiling bitcoin source code"
date: 2017-07-26
categories: ["Blockchain"]
tags: ["bitcoin", "blockchain"]
---

# Compiling bitcoin source code

&gt; git clone https://github.com/bitcoin/bitcoin.git

&gt;cd ~/src/github

&gt;git checkout v0.14.2

&gt;./configure --without-gui --disable-tests --disable-wallet

&gt; make -j 4
