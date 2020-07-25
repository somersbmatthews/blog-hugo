---
title: "WebRTC Architectures using Pion with Go or Golang."
date: 2020-07-23T18:05:36-05:00
draft: true
---

Architectures

# Mesh

   All peers connect directly to all other peers.

# Multipoint Conferencing Unit (MCU)

   All peers connect to a server that handles mixing audio and video into a single stream and forwards it to each peer.

# Selective Forwarding Unit (SFU)

   All peers connect to a server that proxies each stream separately to all the other peers.