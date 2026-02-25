---
title: "Update to Post-quantum Hybrid ECDHE-MLKEM Key Agreement for TLSv1.3"
abbrev: "Hybrid ECDHE-MLKEM Update"
category: std

docname: draft-usama-tls-ecdhe-mlkem-update-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Security"
workgroup: "Transport Layer Security"
keyword:
 - hybrid
 - post-quantum
venue:
  group: "Transport Layer Security"
  type: "Working Group"
  mail: "tls@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/tls/"
  github: "muhammad-usama-sardar/tls-ecdhe-mlkem-update"
  latest: "https://muhammad-usama-sardar.github.io/tls-ecdhe-mlkem-update/draft-usama-tls-ecdhe-mlkem-update.html"

author:
  -
    fullname: "Muhammad Usama Sardar"
    ins: M. Usama Sardar
    organization: TU Dresden
    city: Dresden
    country: Germany
    email: "muhammad_usama.sardar@tu-dresden.de"

normative:
  I-D.ietf-tls-ecdhe-mlkem:
informative:
  RFC9847:
  I-D.ietf-pquip-pqc-engineers:
...

--- abstract

This is a quick update of to-be RFC {{I-D.ietf-tls-ecdhe-mlkem}} for recommending the three hybrid key agreement mechanisms in TLS 1.3.


--- middle

# Introduction

The readers are assumed to be familiar with {{I-D.ietf-tls-ecdhe-mlkem}} and {{RFC9847}}.


## Motivation

Given the risk of "hardvest-now, decrypt-later" attacks {{I-D.ietf-pquip-pqc-engineers}}, we believe that the hybrid key agreement mechanisms need to be recommended.

{{Section 3 of RFC9847}} defines the meaning of "Y" in "Recommended" column as follows:

{:quote}
>  Y:
Indicates that the IETF has consensus that the item is RECOMMENDED. This only means that the associated mechanism is fit for the purpose for which it was defined. Careful reading of the documentation for the mechanism is necessary to understand the applicability of that mechanism. The IETF could recommend mechanisms that have limited applicability but will provide applicability statements that describe any limitations of the mechanism or necessary constraints on its use.

This draft aims to build the mentioned consensus.


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

The security considerations of {{I-D.ietf-tls-ecdhe-mlkem}} apply.


# IANA Considerations

This document requests the following updates to three entries in the [TLS Supported Groups registry](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-8), according to the procedures in {{Section 6 of RFC9847}}.

## SecP256r1MLKEM768

 Recommended:
 : Y

## X25519MLKEM768

 Recommended:
 : Y

## SecP384r1MLKEM1024

 Recommended:
 : Y

| Value | Description        | Recommended |
|-------|--------------------|-------------|
| 4587  | SecP256r1MLKEM768  | Y           |
| 4588  | X25519MLKEM768     | Y           |
| 4589  | SecP384r1MLKEM1024 | Y           |



--- back

# Acknowledgments
{:numbered="false"}

We thank the authors and contributors of {{I-D.ietf-tls-ecdhe-mlkem}} for their work.
We thank Eric Rescorla for this proposal.
We also thank Bas Westerbaan for the initial idea.
