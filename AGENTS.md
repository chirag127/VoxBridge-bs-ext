# VoxBridge-bs-ext agent instructions

## Scope and responsibilities

This repository is the scaffold for local-first video dubbing for Edge and
Firefox. It currently contains documentation and a GPL-3.0 license, not a
buildable browser extension.

- Coordination: keep the repository name, origin URL, and workspace submodule
  registration consistent; preserve unrelated changes and other worktrees.
- Implementation: update only task-owned files and their affected references.
- Review and verification: independently review the latest revision, check the
  documentation and Git metadata, and distinguish passed checks from blockers.

## Repository identity and constraints

- Repository: `chirag127/VoxBridge-bs-ext`; default branch: `main`.
- Workspace location: `repos/own/public/browser-extensions/VoxBridge-bs-ext`.
- The workspace tracks this repository as a submodule, not as copied source.
- Use a separate review branch and the workspace's reviewed-PR process. Do not
  publish unreviewed changes directly to the default branch.
- Preserve the license and the local-first, no-paid-inference-API scope.
- No application dependencies, build command, or runtime test suite is defined.
  Documentation checks do not establish that a browser extension works.

## Verification

With Node.js 22 or newer and the current `origin/main` fetched, run these
commands from this repository:

```sh
npx --yes markdownlint-cli2@0.24.2 README.md AGENTS.md
git diff --check
git diff --cached --check
git diff --check origin/main...HEAD
git remote get-url origin
git ls-files --stage
```

The three diff checks cover unstaged edits, staged edits, and the committed PR
patch, respectively.

The origin must identify `chirag127/VoxBridge-bs-ext` on GitHub. The canonical
workspace URL is `https://github.com/chirag127/VoxBridge-bs-ext.git`; equivalent
HTTPS URLs with or without `.git`, and SSH URLs, are valid. Verify the workspace's
submodule path and URL separately in the owning workspace checkout.

## OKF documentation gap

No repository-specific OKF format or bundle is defined. The workspace requires
OKF documentation in `okf/`, but its format must be established before creating
a bundle. Report this gap; do not invent a format or silently import an obsolete
workspace-wide documentation layout.

<footer class="hire-me">
    <h3>Hire me</h3>
    <p>Chirag Singhal — building free, open APIs and tools.</p>
    <p>
        <a href="mailto:chirag@oriz.in">chirag@oriz.in</a> ·
        <a href="https://github.com/chirag127">GitHub</a> ·
        <a href="https://www.linkedin.com/in/chirag127/">LinkedIn</a> ·
        <a href="https://x.com/singhal127">X</a> ·
        <a href="https://www.youtube.com/@ChiragSinghal127">YouTube</a> ·
        <a href="https://www.instagram.com/chiragsinghal127/">Instagram</a> ·
        <a href="https://www.reddit.com/user/Far_Macaron_9910/">Reddit</a> ·
        <a href="https://buymeacoffee.com/chirag127">Buy me a coffee</a>
    </p>
</footer>
