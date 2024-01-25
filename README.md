# About

This repository contains an example of running Zap augmented by chalk metadata

### Prerequisites

Ensure that you have [a valid PAT token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) and that you have successfully authenticated
with github:

```bash
❯ docker login ghcr.io
Authenticating with existing credentials...
Login did not succeed, error: Error response from daemon: Get "https://ghcr.io/v2/": denied: denied
Username (<your username>):
Password:
Login Succeeded
```

### Performing a Scan

1. Run `docker docker compose up -d dvwa` to bring up the [damn vulnerable web app](https://github.com/digininja/DVWA)
2. Run `docker compose run --rm zap zap.sh -cmd -autorun /zap/wrk/FullScanTech.yaml`
   to trigger a ZAP scan.

### Cleanup

Run `docker compose down` to clean up resources.
