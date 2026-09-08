# Repository instructions

## GitLab and GitHub synchronization

- GitLab is the primary remote: `origin` points to `git@gitlab.com:bbilaniu/bbilaniu.gitlab.io.git`.
- GitHub is the secondary copy: `github` points to `https://github.com/bbilaniu/bbilaniu.github.io.git`.
- The local `main` branch tracks `origin/main`, so a default push targets GitLab.
- Do not assume automatic mirroring. No synchronization job was found in this repository; GitLab's server-side mirror settings have not been verified.
- When asked to push or publish repository changes, keep both remotes updated: run `git push origin main`, then `git push github main`. If either fails, report which remote remains out of sync. Do not force-push to resolve divergence.
- To copy commits already on local `main` to GitHub, use `git push github main`.
- Verify current synchronization with `git ls-remote origin refs/heads/main` and `git ls-remote github refs/heads/main`; matching commit hashes mean their `main` tips match. Local remote-tracking refs may be stale.
- If GitLab SSH authentication is unavailable, its public branch tip can be checked using `git ls-remote https://gitlab.com/bbilaniu/bbilaniu.gitlab.io.git refs/heads/main`.
