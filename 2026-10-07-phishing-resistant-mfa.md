---
layout: default
title: "Phishing-Resistant MFA: A Beginner's Guide"
date: 2026-10-07
tags: [cybersecurity]
---

# Phishing-Resistant MFA: A Beginner's Guide

## What MFA Is

Multifactor authentication (MFA) is a layered way to protect an account. You have to show two or more different kinds of proof before you're let in. Usually that's a password plus something else, like a code on your phone or a physical security key (CISA fact sheet). The point is simple: if someone steals your password, it isn't enough on its own to break in (CISA fact sheet).

CISA's position is that any MFA is better than a password alone. It also stresses that some forms of MFA are much stronger than others, and that attackers have learned to get around the weaker ones (CISA fact sheet).

## How Attackers Get Around Weaker MFA

The fact sheet describes several common attacks.

**Phishing.** An attacker sends an email that leads to a fake login page made to look like a real company site. You type in your username, password, and MFA code, and the attacker captures all of it and uses it to log in as you (CISA fact sheet).

**Push bombing.** Some MFA sends a notification to your phone asking you to approve a login. An attacker who already has your password triggers notification after notification until you approve one, whether by accident or just to make them stop (CISA fact sheet).

**SS7 exploitation.** SS7 is a protocol that phone networks use to route calls and texts. Attackers can abuse weaknesses in it to intercept text-message and voice-call MFA codes (CISA fact sheet).

**SIM swapping.** An attacker convinces your mobile carrier to move your phone number onto a SIM card they control. From then on, your text and call codes go to them instead of you (CISA fact sheet).

All four attacks have the same root weakness. They either trick the user or intercept a code that's sent over the network.

## What "Phishing-Resistant" Means

Phishing-resistant MFA is built so that a fake login page can't capture anything useful, even if the user is fooled into visiting it. CISA calls this the gold standard for MFA and strongly urges organizations to adopt it (CISA fact sheet). The fact sheet names two forms.

### 1. FIDO/WebAuthn

This is the most widely available form of phishing-resistant MFA, and major browsers, operating systems, and smartphones support it (CISA fact sheet). The authenticator comes in one of two kinds:

- **A separate physical token**, such as a security key that plugs in over USB or connects by tapping it to a device using NFC (CISA fact sheet).
- **A built-in authenticator** embedded in a laptop or phone (CISA fact sheet).

### 2. PKI-Based MFA

This form uses smart cards, like the PIV and CAC cards used in the federal government (CISA fact sheet). It's strong, but CISA notes it's less widely available and needs a mature identity-management setup, so it's most common in large organizations and government (CISA fact sheet).

## If You Can't Go Phishing-Resistant Yet

CISA recognizes that not every system can switch right away, so it ranks the other options from strongest to weakest (CISA fact sheet):

1. **App-based push notifications with number matching.** You have to type a number shown on the login screen into the app, which defeats push bombing.
2. **App-based or token-based one-time passwords.**
3. **SMS or voice codes.** These are the weakest, but still better than no MFA at all.

CISA presents these as interim steps, not final answers (CISA fact sheet).

## How Organizations Should Roll It Out

The fact sheet gives practical advice for making the switch:

- **Find out which systems already support it.** Identify which services and applications can use FIDO/WebAuthn or PKI (CISA fact sheet).
- **Protect the most valuable targets first.** Start with the accounts attackers most want, such as system administrators and other privileged users (CISA fact sheet).
- **Plan for legacy systems.** Some older systems can't support phishing-resistant MFA. Organizations should plan to upgrade them or use a stronger interim option until they can (CISA fact sheet).
- **Use single sign-on (SSO).** Connecting applications to a central SSO system that supports phishing-resistant MFA lets one strong login protect many apps (CISA fact sheet).

CISA frames all of this as part of a larger move toward Zero Trust, a security approach where no user or device is trusted automatically and every access request has to prove itself (CISA fact sheet).

## The Takeaway

MFA blocks many attacks, but codes and push approvals can still be phished, intercepted, or spammed. Phishing-resistant MFA, meaning FIDO/WebAuthn or PKI, removes that weakness, and CISA wants organizations moving toward it, starting with their most important accounts (CISA fact sheet).

## Sources

- CISA, [Implementing Phishing-Resistant MFA (fact sheet)](https://www.cisa.gov/sites/default/files/publications/fact-sheet-implementing-phishing-resistant-mfa-508c.pdf)
