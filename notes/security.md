# Security

* minimize attach surface
* secure defaults
* principle of least privilege
* defence in depth
* fail securely
* 0 trust
* separation of duties
* avoid security by obscurity
* keep security simple
* fix security issues correctly
* relaiability is important for security

authentication -> who is the user?
authorization -> can the user do that?

* openId -> authenticate users through an openid provider
  - users are registered with openid provider
  - forward auth requests to provider
  - returns success message and profile on successful login
* oauth 
  - an authorization mechanism that allows the application user access to a provider (gmail, fb etc)
  - on successful response, app receives a token which can be used to access apis on user behalf
  - can be used as a pseudo authentication

ciphers
- stream and block
- summetric key encryption
  * DES - data encryption standard - 52 bit key
  * Triple DES
  * AES - 126,192,256 bit keys
- assymetric key encryption
  * diffie hellman key exchange - exchange symmetric keys securely
  * RSA - public and private key

hashing
* md5
* sha1, sha256

digital signature
- add a signature and sign with private key, can be verified using
  public key
- PKI - public key infrastructure
  - heirarchial framework for managing certs
  - certs are signed by CA
  - CA can be trusted third party or within organization
  - most web browsers have root CA of popular ones by default

CA process
* generate public/private pair
* create cert signing request and forward to CA
* CA approves and signs
* store cert


## Login security

* ssh
  - secure shell
  - authz/authn
  - encrypted
* cert chain
  - end cert -> intermediete cert  (issuer) -> root cert

TLS handshake
* client sends hello with supported protos and algos
* server sends back hello with cert chain and selects cipher
* negotiate a session key
* encrypt using session key

* TLS 1.2 is latest

## Network security

* IPSec -> encryption of ip packets at network layer
  - used by vpns
* PGP/SMIME -> email security
* TLS

## Network perimeter security

* firewalls
* packet filters
  - filters based on ip/tcp headers
* circuit gateways
  - check tcp/ip and port to evaluate whether to allow connection
* DPF -> packet filter + circuit gateways
* ALG - application level gateways (proxy)
  - can do deep inspection on packets
  - works as a proxy
* Bastion hosts -> controlled ingress points to a system


* nmap -> scan ports
* openvas, wireshark

* DNS protection - dnssec
* BGP - border gateway protol - exchange routing info

## Web based attacks

* cross site request forgery - csrf
* cross site scripting - xss
* phishing
* clickjacking
* sql injection

## Security breach

* DOS, DDOS
  - flooding
  - slow norris
* wiretapping
* backdoors
* bruteforce
* dictionary based attacks
* replay attacks
* MITM
* ip spoof, mac spoof
* eavesdropping
* social eng
* Phishing
* dns poisoning

## OWASP top 10

* sql injection
* broken auth
* sensitive data exposure
* xml external entities
* broken access control
* XSS
etc


dont check in secrets to git!

## Docker security

* keep kernel and host up to date
* dont expose docker daemon socket
* dont run as root container
* limit capabilities
* dont run with privileged
* dont allow privilege escalation
* disable inter container communication
* use seccomp, selinux etc
* limit resources
* set fs to readonly and use tempfs
* use sast (snyk)
* dont store secrets
* use trusted images (opa gatekeeper)
* sign and verify docker images
* monitor oss vulnerabilities
* use fixed tags
* use a linter

## Kubernetes security

* secure container images
* secure code and dependencies
* manage configuration securely
* use latest k8s

NASA

* use pod security policy (deprecated)
* use rbac
* limit access to etcd and control planes using firewall
* network policies for pods
* use secrets for sensitive data
* enable audit logging (persist them)
* apply security patches
* run scans
* rootless container engines
* run isolated containers if needed (vm like)
* disble automount serviceaccount token
* use separate serviceaccounts
* use limitrange and quotas
* mTLS in servicemesh
* use sealedsecret/sops or something to secure secrets
