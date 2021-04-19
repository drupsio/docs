# Release Process

## Branches

1. `main` branch for production
2. `develop` branch for active development
3. `feature/[feature-name]` branches for new features
4. `hotfix/[issue-name]` branches for hotfixes

## Release

1. Create release branch from `develop` prefixed by `release/[version]`, for example: `release/1.0.0`
2. Bump version based on release
3. Generate a changelog file
4. Commit all change to release branch with `tag` on it
5. Create a pull request from the release branch to `master`: `release/1.0.0` -> `master`

## HotFixing

### **Case 1**: hotfix needed on `master` branch

1. Crete hotfix branch from `master` prefixed by `hotfix/[issu-name]`, for example: `hotfix/1-fix-user-creation`
2. Fix the issue
3. Bump patch version, so if the version is `1.0.0` it will be bumped as `1.0.1` and commit
4. Commit all change to the hotfix branch
5. Generate changelog file
6. Create a pull request from the `hotfix` branch to `master`: `hotfix/1-fix-user-creation` -> `master`
7. Create a pull request from the `hotfix` branch to `develop`: `hotfix/1-fix-user-creation` -> `develop`

### **Case 2**: hotfix needed on `release/[version]` branch, for example: `release/1.0.0`

1. Pull the related `release` branch: `release/1.0.0`
2. Fix the issue and commit changes
3. Generate changelog file
4. Push changes
5. Create a pull request from the `release` branch to `develop`: `release/1.0.0` -> `develop`
