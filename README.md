# AddressNormalizationService

Just an example of an http server in Node with an odd project name.

## Running

```bash
git clone https://github.com/hoopdad/addressnormalizationservice.git
cd addressnormalizationservice
npm start
```

## Security posture

The server is implemented using Node's built-in `http` module — **no external npm dependencies** — so there is no npm vulnerability surface area to worry about.

### Self-fixing process

Two layers of automated security maintenance are in place:

1. **Dependabot** (`.github/dependabot.yml`) — opens weekly pull requests to update any npm packages or GitHub Actions that are added in the future.

2. **Security Audit workflow** (`.github/workflows/security.yml`) — runs on every push to `main` and on a weekly schedule (Mondays 06:00 UTC). If `npm audit` reports vulnerabilities it automatically runs `npm audit fix --force`, commits the updated `package.json` / `package-lock.json`, and pushes the fix back to `main`.

