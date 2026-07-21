# Agent Security Lab
This repository contains artifacts related to my practicum project for Georgia Tech's Master of Science in Cybersecurity program. The research paper is located at the root level of this repository and is titled "Distributing Security Controls Through Harness Engineering". 

## Abstract
AI coding agents are being adopted at historic speed, yet security and risk concerns remain the primary barrier to scaling agentic AI across organizations. Existing security controls for coding agents are not systematically distributed to engineering teams, and vendor-native solutions introduce ecosystem dependencies that may not suit every deployment context. This paper investigates whether off-the-shelf security controls can be implemented on commercial AI coding agents and scaled to a distributed user base via a custom agent harness. A phased testing methodology was applied across four agent configurations — two commercial agents with and without controls,
a baseline harness, and a security-hardened harness — using a 23-test suite derived from the OWASP Top 10 for Agentic Applications. SHarD (Secure Harness Distribution), a distributable harness built on the Pi agent harness, demonstrated that three categories of security controls — OS sandboxing, skill scanning, and tool restriction — can be embedded and distributed via a single install command while retaining equivalent efficacy to
direct installation on commercial agents. SHarD achieved an adjusted score of 100%, matching the best securely configured commercial agent, with no regression across any test category. Notable observations include evidence that model non-determinism produces inconsistent security outcomes and that autonomous agent behavior can cross system boundaries in ways that OS sandboxing directly mitigates. Initial characteristics toward a
control harness fitness framework are proposed, and a third research question is identified for future investigation.

## Artifacts
SHarD or Secure Harness Distribution is built on the framework provided by [Pi Coding Agent](https://github.com/earendil-works/pi).The demo code, which was used for the research, can be found at [github.com/wrgore/shard-demo](https://github.com/wrgore/shard-demo).

The early beta version of SHarD can be found at [github.com/wrgore/shard](https://github.com/wrgore/shard).

The prod folder contains test files. The prompt injection attempts here are benign and for testing purposes only. Additionally, the credentials located in these files are not real.

The data folder contains the raw test results in JSON format. 

The tests folder contains a markdown file of the 23 tests used to evaluate the basic functionality of security controls for AI coding agents.
