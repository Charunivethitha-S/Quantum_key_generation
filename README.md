# Quantum-Enhanced Post-Quantum Secure Cryptographic Hardware

This project presents a quantum-enhanced cryptographic hardware architecture designed for next-generation embedded systems. The system integrates quantum randomness, post-quantum cryptography, secure key derivation, and high-speed encryption to build a future-proof security pipeline.

**The architecture is designed for FPGA-based implementation and demonstration in hardware security research and hackathons**

# Project Overview

Traditional cryptographic systems rely on pseudo-random number generators and classical key exchange methods that may become vulnerable with the development of quantum computers. This project introduces a multi-layer secure architecture that combines:
 - Quantum Random Number Generation

 - Post-Quantum Key Exchange

 - Cryptographic Key Whitening

 - High-speed Stream Cipher Encryption


**The goal is to create a secure keystream generator for embedded systems and IoT devices**.


# System Architecture

The system follows this pipeline:

 - Photon Arrival QRNG
 - Input Keying Material (IKM) Generation
 - Post-Quantum KEM
 - HKDF Cryptographic Whitening
 - Quantum-Inspired Encryption Engine
 - Secure Keystream Output

**Each stage strengthens the security of the generated key before encryption**.

# Module Description

 - Quantum Random Number Generator (QRNG)

The QRNG module generates entropy based on photon arrival randomness. Quantum phenomena ensure the generated bits are unpredictable and suitable for cryptographic applications. In the hardware prototype, a random bit stream is generated and accumulated to form the base entropy source.

- Input Keying Material (IKM) Generation

Random bits from the QRNG are collected into a fixed-size block (256-bit). This block becomes the initial entropy used for secure key generation. This stage ensures sufficient randomness is gathered before further cryptographic processing.

- Post-Quantum Key Exchange

The architecture integrates a post-quantum key encapsulation mechanism based on CRYSTALS-Kyber. This protects the system against attacks from future quantum computers by using lattice-based cryptographic security. The generated shared secret strengthens the entropy before key derivation.

- HKDF Cryptographic Whitening

The HKDF stage performs entropy extraction and removes statistical bias from the input keying material.

This stage:

1.Mixes entropy

2.Eliminates correlations

3.Produces a uniform cryptographic key

This ensures strong cryptographic key quality.

 - Quantum-Inspired Encryption Engine

The final encryption stage is based on ChaCha20. The engine performs high-speed permutation operations using ARX operations:

 1. Addition

 2. Rotation

 3. XOR

This generates a secure keystream suitable for encrypting sensitive data in embedded environments.


# Features

* Quantum-based entropy generation

* Post-quantum cryptographic security

* Hardware-friendly design

* Multi-layer security architecture

* FPGA implementation support

* Secure keystream generation

* Suitable for IoT and embedded systems

#  Technologies Used

* Verilog HDL

* FPGA Development Boards

* Hardware Simulation (ModelSim / EDA Playground)

* Post-Quantum Cryptography

* Stream Cipher Architecture

# Applications

* Secure IoT devices

- Embedded system security

* Defense communication systems

- Secure hardware accelerators

* Next-generation cryptographic processors


# Future Improvements

* Full hardware implementation of Kyber accelerator

* Real photon-based QRNG hardware integration

* ASIC implementation

* Performance optimization

* Side-channel attack resistance

# Project Goal

To demonstrate a future-ready cryptographic hardware system that combines quantum entropy and post-quantum algorithms for secure and efficient data protection.


---

If you want, I can also write a very strong GitHub version that looks like a research project (which helps during hackathon judging and recruiter reviews).
