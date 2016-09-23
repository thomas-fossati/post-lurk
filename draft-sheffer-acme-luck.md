---
title: The ACME LUCK (Limited Use of Cached Keys) Protocol
abbrev: ACME LUCK
docname: draft-sheffer-acme-luck-latest
date: 2016-09-17
category: std

ipr: trust200902
area: Security
workgroup: ACME Working Group
keyword: Internet-Draft

stand_alone: yes
pi: [toc, sortrefs, symrefs]

author:
 -
    ins: Y. Sheffer
    name: Yaron Sheffer
    organization: Intuit
    email: yaronf.ietf@gmail.com
 -
    ins: D. Lopez
    name: Diego Lopez
    organization: Telefonica I+D
    email: diego@telefonica.es
 -
    ins: T. Fossati
    name: Thomas Fossati
    organization: Nokia
    email: thomas.fossati@nokia.com

normative:
  RFC2119:
  I-D.ietf-acme-acme:

informative:
  I-D.iab-web-pki-problems:

--- abstract

This memo describes the ACME LUCK (Limited Use of Cached Keys) protocol.  LUCK allows a domain owner to delegate to some other entity (e.g., a CDN edge cache) the authority to terminate TLS connections on its behalf, using short-term certificates.  These certificates allow the domain owner to revoke the TLS server's authorization when necessary, without requiring certificate revocation.

--- middle

# Introduction

Content owners frequently prefer a Content Delivery Network (CDN) to distribute their content.  CDNs typically have very large footprint, which allows them to serve content to a global audience with a high aggregate bandwidth and low latency.  To protect this traffic, the CDN uses HTTPS and presents a certificate that usually bears the content owner's name.  However, many content owners balk at sharing their long-term private keys with another organization.

This memo describes the ACME LUCK (Limited Use of Cached Keys) protocol. LUCK extends ACME {{I-D.ietf-acme-acme}} to automate the generation and renewal of short-term certificates that a third party server  (e.g., a CDN edge cache), which has been explicitly authorized by the legit content owner, can use to serve content using that content owner's domain name.

The content owner can revoke the third party’s authorization when necessary by instructing the ACME server to stop the automatic certificate refresh and let the active certificate expire (e.g., after a few hours).   Note that, by enforcing the use of short-term certificates, LUCK doesn’t rely on explicit certificate revocation in order to work (see section 3.2.1 of {{I-D.iab-web-pki-problems}}).

# Conventions used in this document

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in {{RFC2119}}.

The following terms are used to identify the LUCK protocol actors:

- Content Owner: the owner of a domain name that uses a third party to deliver its content via HTTPS.
- TLS server: the node delegated by the Content Owner to terminate the TLS connection (typically a CDN edge cache).  During TLS handshake it offers its clients a certificate bearing the Content Owner's name.
- ACME LUCK Server: an ACME server that also exposes LUCK interfaces to the Content Owner to boostrap and terminate the delegation, and to the TLS server to serve the automatically refreshed certificates.


# Protocol Flow

## Bootstrap

~~~~~~~~~~
TODO
~~~~~~~~~~
{: #figprotoboot title="Bootstrap"}


## Refresh

~~~~~~~~~~
TODO
~~~~~~~~~~
{: #figprotorefresh title="Refresh"}


## Termination

~~~~~~~~~~
TODO
~~~~~~~~~~
{: #figprototerm title="Termination"}

# Security Considerations

TODO security considerations

--- back


# Examples

This appendix provides some examples of the ACME LUCK protocol operation.

~~~~~~~~~~
TODO
~~~~~~~~~~
{: #figexample title="Example 1"}
