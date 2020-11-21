---
layout: post
title:  "Internet Security"
subtitle:   "Internet Security"
categories: junk 
tags: Internet
comments: false
---

## 개요
> `Internet Security`에 대해 알아본다.

### Internet Security Intro

Computer/System security

- data in a computer

Network security

- **trainsmission of information**

eavesdrop

Tamper

impersonation

hijacking

denial of service

### Attacks

Malware
- Virus
- Worm
- Trojan horse
- Adware
- Spyware
    - keylogger
- Ransomware

Spam
Buffer overflow

Denial of service
Network-based attacks
Physical attacks

Password attacks
Information gathering attacks
Side channel attacks

network-baed attacks

cryptographic attacks
spoofing
session hijacking
passive attacks
- wiretapping
- port scanner
active attacks
- DDos
- spoofing
- tampering
- man in the middle
- poisoing


### Security Services

Confidentiality : 기밀성
- tapping
- traffic analysis
Integrity : 무결성
- Modification
- Masquerading
- Replaying
- Repudiation
Availability : 가용성
- DoS
+)
Authentication : 인증
Non-repudiation : 부인방지

Access control
- identification : 신분
- authentication : 인증
- authorization : 권한

Anonymity
Accountability
Privacy
Digital forensics

**Security mechanisms**
- Encryption/ Decryption
- key
- confidentiality(비밀보호), authentication(입증)

Message digest
- Hash function
    - integrity(무결성)
Digital Signatures
- Authentication, integrity, non-repudiation

Append-only public server (Blockchain)

Symmetric cryptography(비대칭 암호화)
    - single key
Publick key cryptography(공개키)
    - two keys

Block cipher (암호화가 block 단위로)
Stream cipher (1 bit 단위로)

### Threat Modeling

definition
: Threat modeling is the process of systematically identifying the threats of a given system
1. Identify things of value that you want to protect
2. Enumerate the attack surfaces
3. Hypothesize attackers and map them to - 공격자 추정
    Things of value they want from (1)
    Their ability to target vulnerable surfaces from (2)
4. Survey mitigations
5. Balance costs versus risks

PII : Personally identifiable information 

