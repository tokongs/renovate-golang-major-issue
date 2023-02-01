# renovate-golang-major-issue
The issue occurs when multiple Go dependencies have major upgrades at the same time.
All dependencies will get their path updated with the first dependency's major version, not their own.

## To recreate
1. Install two Go dependencies with outdated major versions. 
2. Import them in a Go file
3. Group golang updates in renovate.jon
4. Enable `gomodUpdateImportPaths` in `postUpdateOptions`
5. Watch things break when renovate tries to update multiple major versions
