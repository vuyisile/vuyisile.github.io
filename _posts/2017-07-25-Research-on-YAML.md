---
layout:
title:	Research on YAML
date:	2017-07-25
---

### What is YAML?


**YAML** is a human-readable data serialization language. Serilization-is the process of translating data structures or object state into a format that can be stored.

It is used for ***configuration files***, and could be used in many applications where data is being stored or transmitted. 

YAML targets many of the same communications applications as XML, but has taken a more minimal approach which intentionally breaks compatibility with SGML(Standard Generalized Markup Language- a standard for defining generalized markup languages for documents).

YAML 1.2 is a superset of JSON (JavaScript Object Notation), another minimalist data serialization format where braces and brackets are used instead of indentation.

Custom data types are allowed, but YAML originally encodes scalars (such as strings, integers, and floats), lists, and associative arrays (also known as hashes or dictionaries). These data types are based on the Perl programming language, though all commonly used high-level programming languages share very similar concepts. YAML supports both Python-style indentation to indicate nesting, and a more compact format that uses **[]** for lists and **{}** for hashes. The colon-centered syntax used to express key/value pairs is inspired by electronic mail headers as defined in RFC 0822, and the document separator **"--"** is borrowed from MIME (RFC 2045). Escape sequences are reused from C, and whitespace wrapping for multi-line strings is inspired from HTML. Lists and hashes can contain nested lists and hashes, forming a tree structure; arbitrary graphs can be represented using YAML aliases (similar to XML in SOAP). YAML is intended to be read and written in streams, a feature inspired by SAX.

Support for reading and writing YAML is available for several programming languages. Some source code editors such as Emacs and various integrated development environments have features that make editing YAML easier, such as folding up nested structures or automatically highlighting syntax errors.
