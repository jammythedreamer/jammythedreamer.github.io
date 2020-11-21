---
layout: post
title:  "Symmetric Cryptography"
subtitle:   "Symmetric Cryptography"
categories: junk 
tags: Cryptology
comments: false
---

## 개요
> `Symmetric Cryptography`에 대해 알아본다.

plain text
cipher text
shared key
encryption cipher
decryption cipher

What is strong encrythion algorithm?

Diffusion : plain text 를 조금 마꾸면 cipher text는 마구 바뀌어야한다.
Confusion : key 와 cipher text와의 관계가 추정하기 어려워야한다.

How make strong encrytion algorithm

- Substitution cipher (대치 암호)

    one or more characters replace to ciphertext by fixed mapping system
    monoalphabetic
    polyalphabetic

    modulo operation

    Caesar cipher

    frequncy analysis
- Permutation/transportation cipher (전치 암호)
    
    순서를 바꿈

    columnar cipher


- exclusive-or cipher

    X-OR
    addition modulo 2

## DES and AES

**DES**

64 bit -> 64 bit
key 56 bit + 8 parity

**AES**

128 bit -> 128 ->

key 128, 192, 256
rount 10, 12 ,14

16bytes -> 4 x 4 matrix

SubBytes
ShiftRows
MixColumns
AddRoundKey
