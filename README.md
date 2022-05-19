# Trusted-Third-Party-Multi-Key-Exchange-Protocol-using-Elliptic-Curve-Diffie-Hellman-Cryptography-

The section includes a tutorial video captured in explanation to the implementation of Trusted Third party Multi key exchange protocol using Elliptic Curve Cryptography based on Diffie Hellman

# Introduction
•	Elliptic-curve cryptography (ECC) is a public-key cryptography technique. 
•	Elliptic curves are applicable for key agreement, digital signatures, pseudo-random generators and other tasks.
•	Elliptic curve is a plane algebraic curve defined by an equation of the form y2  = x3+ax+b .  
•	Elliptic-curve Diffie–Hellman (ECDH) is an anonymous key agreement protocol that allows two parties, each having an elliptic-curve public–private key pair, to establish a shared secret over an insecure channel.
•	This shared secret may be directly used as a key, or to derive another key.

![image](https://user-images.githubusercontent.com/30871627/169285881-2c6cdcdc-e92e-4fc8-a6a8-d840e31e2cdc.png)

The following explains the implementation part,

1. Alice wants to establish a shared key with Bob, but the only channel available for them may be eavesdropped by a third party. 
2. Initially, the domain parameters (that is, (p,a,b,G,n,h) in the prime case or (m,f(x),a,b,G,n,h) in the binary case) must be agreed upon. Also, each party must have a key pair suitable for elliptic curve cryptography, consisting of a private key d (a randomly selected integer in the interval [1, n-1] and a public key represented by a point Q (where Q = d G, that is, the result of adding G to itself d times).

![image](https://user-images.githubusercontent.com/30871627/169286008-ffd47145-99d9-4c7a-8f42-adc260a1fede.png)

3. Let Alice's key pair be (d_A, Q_A) and Bob's key pair be (d_B, Q_B). Each party must know the other party's public key prior to execution of the protocol.
4. Alice computes point (x_k, y_k) = d_A Q_B. Bob computes point (x_k, y_k) = d_B Q_A. The shared secret is x_k (the x coordinate of the point). Most standardized protocols based on ECDH derive a symmetric key from x_k using some hash-based key derivation function.
5. The shared secret calculated by both parties is equal, because d_A Q_B = d_A d_B G = d_B d_A G = d_B Q_A.
6. 
![image](https://user-images.githubusercontent.com/30871627/169285532-65ba25d4-f1c8-4fee-b60e-a75fbce2e8a7.png)

The only information about her private key that Alice initially exposes is her public key. So, no party other than Alice can determine Alice's private key, unless that party can solve the elliptic curve discrete logarithm problem. Bob's private key is similarly secure. No party other than Alice or Bob can compute the shared secret, unless that party can solve the elliptic curve Diffie–Hellman problem.

# The Elliptic Curve Digital Signature Algorithm

![image](https://user-images.githubusercontent.com/30871627/169286692-ee5654fd-5bb6-4b59-a8df-28f6885d62d7.png)

# Why Elliptic Curve Cryptography

1. Relatively, easy to perform but extremely difficult to reverse as it leads to Discrete Logarithm Problem.
2. Private keys are generated for only for one single session and thrown away afterwards.
3. A 256-bit/ 164-bit ECC security have an equivalent security attained by 3072-bit/ 1024-bit RSA cryptography.
4. Short key is faster and requires less computing power than other first- generation encryption public key algorithms.
5. Until the cryptanalyst has the private key of the receiver the message is not revealed. Applying Brute Force attack could take years to solve as key size is very large. 

Note: If you find this concept interesting, then please find the implementation of the concept below with detailed explanation.
https://drive.google.com/file/d/0B3KPpHv8FGVCRENZcWhZRnhfM3M/view?usp=sharing&resourcekey=0-jyruG2aHpJekslLPFVPxzQ



