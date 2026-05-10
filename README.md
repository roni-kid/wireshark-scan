# Wireshark Packet Analysis Project
**Cybersecurity Domain — Dissecting Packets: From HTTP to TLS**

---

## What This Is

A hands-on packet analysis exercise using Wireshark. The goal was to capture and interpret real network traffic across three protocols — HTTP, DNS, and TLS — and document what each one actually reveals about how data moves (and how exposed it can be).

---

## What's Included

| File | Description |
|---|---|
| `Wireshark_Project.docx` | Full report with screenshots, packet analysis, and findings |
| `capture.pcap` | Raw Wireshark capture file from the exercise |
| `README.md` | This file |

---

## What Was Captured

**HTTP GET** — Plain-text requests to neverssl.com. Every header visible, no encryption.

**DNS** — Query and response for domain resolution over UDP port 53. Includes an anomaly: repeated lookups for the same domain within seconds.

**TLS Handshake** — Client Hello and Server Hello from an HTTPS connection to google.com. Cipher suite negotiated: `TLS_AES_256_GCM_SHA384`.

---

## Tools Used

- Wireshark (capturing on `eth0`)
- Display filters: `http.request.method == "GET"`, `dns`, `tls`

---

## Submitted

10 May 2026
