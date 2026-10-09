# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/commit-boost-client`
Branch: `main`
Inspected head: `273a503178f9987380ea33ddb8b674516ff29601`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/ci.yml` — original Git object `9fde3899d3f560ae99e06cb29d0db7d3c74cb350`.
- `.github/workflows/docs.yml` — original Git object `d6e8f0f86ffbfb22cff1cdc0772d00829b179eda`.
- `.github/workflows/release.yml` — original Git object `4d70eedc7c53b10a0b2ad1d4f48340357a06d355`.
- `.github/workflows/test-docs.yml` — original Git object `c4d18bdfa8987e7ec9c55cef2923a682f22db3cd`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
