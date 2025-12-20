# Releasing

1. Bump the version in `package.json`.
2. Commit and push the change.
3. Create a tag in the form `vX.Y.Z`.
4. Push the tag to GitHub.

The GitHub Actions workflow publishes the VSIX to both the VS Code Marketplace and Open VSX, then creates a GitHub Release with the VSIX attached.
