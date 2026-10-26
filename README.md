# Hands-On Ubuntu Server 26.04 LTS

**Learning and Using Ubuntu Server in the AI Era** · by Henry Hans · First Edition, 2026

<img src="cover.jpg" alt="Cover of Hands-On Ubuntu Server 26.04 LTS" width="280" align="right">

> AI can write the command. Only practice tells you whether it's right.

This is the companion repository for *Hands-On Ubuntu Server 26.04 LTS*. Every procedure in the book was carried out step by step on Ubuntu Server 26.04 LTS, and wherever reality disagreed with the documentation, the book reports what actually happened and how to fix it. This repository keeps that promise going after publication: confirmed errata, updates for newer software versions, and a place to report problems.

- **Paperback:** Amazon (link added at launch) · ISBN 979-8-16-385308-3 · 342 pages, 7.5 × 9.25 in
- **Errata:** [ERRATA.md](ERRATA.md)
- **Updates for newer software versions:** [UPDATES.md](UPDATES.md)
- **Report a problem:** [open an issue](../../issues/new/choose)

<br clear="right">

## What's in the Book

| Part | Chapter |
|---|---|
| **Foundation** | 1. Server Storage and Deploying Ubuntu Server |
| | 2. Ubuntu Server: From Boot to Network Configuration |
| | 3. Ubuntu Server: From System Management to Shutdown |
| **Services** | 4. Compiling Applications from Source, All the Way to the Linux Kernel |
| | 5. Nginx: Enterprise Web Deployment and Management |
| | 6. MySQL, the World's Most Popular Open Source Database, and High Availability |
| | 7. Building an Apache Tomcat Application Server |
| **Scaling out** | 8. KVM: Enterprise-Grade Virtualization |
| | 9. Server Clusters: High Availability and Load Balancing in Practice |
| | 10. Docker Containers and Kubernetes Clusters |
| | 11. AI Servers: Training a Local Large Language Model |
| **Security** | 12. Hardening the Server System and Its Highest-Traffic Network Services |

## Tested Versions

Ubuntu Server 26.04 LTS with the Linux 7.x kernel, Nginx 1.28, MySQL 8.4 LTS, PHP 8.5, OpenJDK 25, Tomcat 10.1 and 11, Kubernetes 1.35, and the NVIDIA 595 server driver series. When a version used in the book is superseded, the change is recorded in [UPDATES.md](UPDATES.md).

## Lab Environment

You can follow the whole book with a single physical host and a handful of virtual machines.

| Requirement | Used for |
|---|---|
| One machine running Ubuntu Server 26.04 LTS | Chapters 1–7 and 12 |
| 2–4 virtual machines (2 vCPU, 2–4 GB RAM each) | MySQL replication (Ch. 6), clusters (Ch. 9), Kubernetes (Ch. 10) |
| Nested virtualization enabled | KVM (Ch. 8), if you run it inside a VM |
| An NVIDIA GPU (8 GB VRAM or more) | Local LLMs with Ollama (Ch. 11) |

The examples use the private network `10.0.0.0/24`, with a server's second, internal NIC on `10.0.1.0/24`, and interface names such as `ens33`. Substitute your own addresses and interface names wherever they appear.

**If you build the lab from cloned VMs**, give every clone its own hostname, regenerate `/etc/machine-id`, and assign a unique static IP *before* you configure any service. Duplicate hostnames and machine IDs cause some of the most confusing failures in Chapters 9 and 10 (see the Tips boxes there).

## Reporting a Problem

If a command no longer works on a current system, please [open an issue](../../issues/new/choose) and include:

1. The page number and section (for example, *p. 283, Section 11.1.4*).
2. The exact command you ran.
3. What you expected to happen.
4. What actually happened, including the full error message.
5. Your environment: Ubuntu version (`lsb_release -a`), kernel (`uname -r`), and the package version if relevant.

In keeping with the spirit of the book, every reported problem is reproduced in the lab before it is corrected.

## Errata Bounty

Every command in this book was tested, but software changes and mistakes happen. If you report an error and it is confirmed and fixed:

- Your name is listed in [ERRATA.md](ERRATA.md) and printed in the acknowledgments of the next printing (unless you prefer to stay anonymous).
- You receive a free eBook copy of the author's next title.

Rewards are for confirmed errors only and are never tied to reviews.

## Using the Code Examples

You may use the commands, configuration files, and scripts from the book in your own systems, scripts, and documentation without asking for permission. Permission is required only to reproduce a substantial portion of the book itself. Attribution is appreciated but not required: "*Hands-On Ubuntu Server 26.04 LTS* by Henry Hans. Copyright 2026 Henry Hans."

## Contact

- Email: henry.hans.author@gmail.com
- X: [@Henry_Hans_Auth](https://x.com/Henry_Hans_Auth)
