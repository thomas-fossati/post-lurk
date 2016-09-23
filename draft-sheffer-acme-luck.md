---
title: The ACME LURK Protocol
abbrev: ACME LURK
docname: draft-sheffer-acme-lurk-latest
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
    organization: Telefonica
    email: diego@telefonica.es
 -
    ins: T. Fossati
    name: Thomas Fossati
    organization: Nokia
    email: thomas.fossati@nokia.com

normative:
  RFC2119:


--- abstract

TODO abstract

--- middle

Use Cases
=========

TODO use cases

Basic Protocol Flow
===================

~~~~~~~~~~


        STuPiD   ```````````````````````````````,
        Script   <----------------------------. ,
                                              | ,
          ^ ,                                 | ,
          | ,                                 | ,
    (1)   | ,                                 | ,  (3)
    POST  | ,                                 | ,  GET
          | ,                                 | ,
          | v                                 | v

        Peer A   ----------------------->   Peer B
                           (2)
                       out-of-band
                       Notification
~~~~~~~~~~
{: #figproto title="ACME LURK Protocol Flow"}


Security Considerations
=======================

TODO security considerations

--- back


Examples
========

This appendix provides some examples of the ACME LURK protocol operation.

~~~~~~~~~~
TODO
~~~~~~~~~~
{: #figexample title="Example 1"}
