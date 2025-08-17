# Branching Strategy (Git Flow)

We are using **Git Flow**, a branching strategy for managing features, releases, and hotfixes.

## Branch Types
- **main**: Production-ready code.
- **develop**: Integration branch for the next release.
- **feature/***: New features (branched from `develop`, merged back into `develop`).
- **release/***: Prepares a release (branched from `develop`, merged into both `main` and `develop`).
- **hotfix/***: Urgent fixes on production (branched from `main`, merged into both `main` and `develop`).

## Workflow
1. Create `develop` branch from `main`.
2. For new features:
   - Create `feature/*` branch from `develop`.
   - Implement, test, and open PR into `develop`.
3. For releases:
   - Create `release/*` branch from `develop`.
   - Fix bugs, finalize version, and open PR into both `main` and `develop`.
4. For hotfixes:
   - Create `hotfix/*` branch from `main`.
   - Fix the issue, open PR into both `main` and `develop`.

## Example
- Feature branch: `feature/add-login-page` → merged into `develop`.
- Release branch: `release/1.0.0` → merged into `main` and `develop`.
- Hotfix branch: `hotfix/fix-title` → merged into `main` and `develop`.
