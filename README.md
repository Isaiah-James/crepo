# CREO — Repository Index (CREPO)

This repository is the **canonical index and structural map of the CREO ecosystem**.

CREPO is **not a monorepo** and is **not intended to be built or run directly**.  
Instead, it exists to expose the *high-level organization, boundaries, and responsibilities* of CREO’s major systems in a transparent and intentional way.

Some subsystems are public, others are private.  
This is **by design**.

---

## Purpose

CREO is a large, multi-system ecosystem composed of independently developed and deployed services, applications, and runtimes.

CREPO exists to:

- Document how CREO is organized at a system level
- Make architectural boundaries explicit and visible
- Provide clear entry points into public development
- Avoid the illusion of a tightly-coupled monolith
- Serve as a navigational reference for contributors, reviewers, and partners

If you are looking for a specific system, SDK, or OpenSource project, this repository tells you **where it lives** and **what it is responsible for**.

---

## Repository Layout

CREPO uses **Git submodules** to represent first-class systems within the CREO ecosystem.

Each submodule is an independent repository with its own lifecycle, tooling, CI/CD, and contribution model.

| Submodule | Visibility | Description |
|---------|-----------|-------------|
| `CREO-Frontend` | Private | Main web application and user interface |
| `CREO-Backend` | Private | Core APIs, domain logic, identity, and services |
| `CREO-RTL` | Private | Real-time layer (eventing, messaging, presence, signaling) |
| `CREO-Praetor` | Public | Local runtime, client shell, and device-level orchestration |
| `CREO-OSS` | Public | OpenSource SDKs, tools, and community projects |

> ⚠️ Private submodules are intentionally inaccessible to the public.
> Attempting to initialize them without permission will fail.

---

## Cloning Behavior (Important)

### Public users
```bash
git clone https://github.com/creo/crepo.git
