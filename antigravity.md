# antigravity.md

## What changed
- Improved package download reliability with progress updates, redirect handling, and timeouts.
- Added CI validation workflow for config consistency.
- Documented architecture, security policy, changelog, and future planning items.

## Files touched (by area)
### Download logic
- `src/main/helper.js`
- `src/config/app.json`

### Automation / CI
- `.github/workflows/ci.yml`

### Documentation
- `README.md`
- `ARCHITECTURE.md`
- `SECURITY.md`
- `CHANGELOG.md`
- `RELEASE_NOTES_DRAFT.md`

### Planning
- `Future-Upgrades.csv`
- `Future_Implements.csv`

## How to run tests/build
```sh
python scripts/test_items.py --no-path --no-lookup --no-url --no-download --no-version
```

Build commands (Windows-focused):
```sh
bash init.sh
bash run.sh
bash build.sh
```

## Follow-ups / risks
- Consider adding retries/backoff to downloads for flaky networks.
- Decide on release cadence and tagging strategy before cutting a release.

## Current repo status
✅ Passing (config validation script run successfully).
