# SBQA Instances and Results Repository

This repository stores paper artifacts:
- `instances/` for problem instances
- `results/` for experiment outputs

Large files are handled with Git LFS.

## Current LFS Policy

Anything under these folders is tracked by Git LFS:
- `instances/**`
- `results/**`

See `.gitattributes` for the active rules.

## Typical Workflow

1. Add files:

```bash
git add instances/ results/
git commit -m "Add new instances/results"
```

2. Verify LFS-tracked files:

```bash
git lfs ls-files
```

3. Push to remote:

```bash
git push
```

## First Push Setup

```bash
git remote add origin <YOUR_REMOTE_URL>
git push -u origin main
```

Make sure your hosting provider supports Git LFS and has enough quota for your dataset size.

## Useful Commands

Track another pattern with LFS:

```bash
git lfs track "*.bin"
git add .gitattributes
git commit -m "Track .bin files via LFS"
```

If a large file was committed without LFS, migrate history before publishing:

```bash
git lfs migrate import --include="path/to/file"
```
