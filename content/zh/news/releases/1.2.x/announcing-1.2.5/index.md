---
title: Announcing Istio 1.2.5
linktitle: 1.2.5
subtitle: Patch Release
description: Istio 1.2.5 patch release.
publishdate: 2019-08-26
release: 1.2.5
aliases:
    - /zh/about/notes/1.2.5
    - /zh/blog/2019/announcing-1.2.5
    - /zh/news/2019/announcing-1.2.5
    - /zh/news/announcing-1.2.5
---

We're pleased to announce the availability of Istio 1.2.5. Please see below for what's changed.

{{< relnote >}}

## Security update

Following the previous fixes for the security vulnerabilities described in [ISTIO-SECURITY-2019-003](/zh/news/security/istio-security-2019-003/)
and [ISTIO-SECURITY-2019-004](/zh/news/security/istio-security-2019-004), we are now addressing the internal control plane communication surface.
These security fixes were not available at the time of our previous security release, and we considered the control plane gRPC surface to be harder to exploit.

You can find the gRPC vulnerability fix description on their mailing list (c.f.
[HTTP/2 Security Vulnerabilities](https://groups.google.com/forum/#!topic/grpc-io/w5jPamxdda4)).

## Bug fixes

- Fix an Envoy bug that breaks `java.net.http.HttpClient` and other clients that attempt to upgrade from `HTTP/1.1` to `HTTP/2` using the `Upgrade: h2c` header ([Issue 16391](https://github.com/istio/istio/issues/16391)).
- Fix a memory leak on send timeout ([Issue 15876](https://github.com/istio/istio/issues/15876)).