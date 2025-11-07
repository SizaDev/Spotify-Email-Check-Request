# Spotify E‑mail Check Request

This repository contains a Python script that sends a request to Spotify's **Account Recovery Magic Link** endpoint.  
It generates random client and device IDs, submits the email, and prints the HTTP status code returned by Spotify.

---

## Features
- Random `X-Client-Id` and `deviceId` per run.
- Single POST request to `/accountrecovery/v3/magiclink/`.
- Prints the server’s status code.

---

## Requirements
- Python 3.8+
- `requests`

Install:
```bash
pip install requests
```

---

## Usage
Edit the `emailOrUsername` field in the script, then run:

```bash
python main.py
```

Example output:
```
Status: 200
```

---

## Status codes
- **200** → Accepted (email likely registered, magic link flow triggered).  
- **400/404** → Not accepted (invalid or not registered).  
- **429** → Rate limited.  
- **5xx** → Server error.

---

## Contact
[![Telegram](https://img.shields.io/badge/Telegram-@SizaGod-blue?logo=telegram)](https://t.me/SizaGod)
