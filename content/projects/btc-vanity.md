---
title: btc-vanity
draft: false
tags:
  - Bitcoin
  - BitcoinWallet
  - Cryptography
  - Rust
  - Vanity
  - BitcoinAddress
---
[[https://github.com/Emivvvvv/btc-vanity|btc-vanity]] is A Bitcoin vanity address generator is written with the Rust programming language.

### What is a vanity address?

A Vanity Address is **a special address that contains a specific pattern or word**. For example, the Vanity Address of a Bitcoin belonging to a user may contain a pattern or word such as "1BTC" or "1Emiv". Vanity Addresses are often used personally or for promotional purposes.

### What btc-vanity can do?

With btc-vanity, you can find a private key that has a compressed Bitcoin pay address that has a custom prefix, suffix, or a string at somewhere in the address.

You can easily run the btc-vanity terminal application locally or use it as a library to create your vanity keypair securely.

### Calling btc-vanity as a library

```rust
 use btc_vanity::vanity_addr_generator::{VanityAddr, VanityMode};  
  
 let vanity_address = VanityAddr::generate(  
             "Emiv", // the string that you want your vanity address to include.  
             16, // number of threads  
             false, // case sensitivity (false ex: eMiv, true ex: Emiv)  
             true, // fast mode flag (set false to use a string longer than 4 chars)  
             VanityMode::Anywhere, // vanity mode flag (prefix, suffix, anywhere available)  
             ).unwrap(); // this function returns a result type  
  
 println!("private_key (wif): {}\n\  
           public_key (compressed): {}\n\  
           address (compressed): {}\n\n",  
                 vanity_address.get_wif_private_key(),  
                 vanity_address.get_comp_public_key(),  
                 vanity_address.get_comp_address())
```

### Examples of usage from terminal

install btc-vanity with cargo
```
cargo install btc-vanity
```
and then you can see possible usage with command
```
btc-vanity -h
```
here are some example screenshots

![example](example.png)
![examples-input-file](examples-input-file.png)