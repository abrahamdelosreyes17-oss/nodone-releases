# Release process

1. Bump `VERSION` in the NodOne repo (e.g. `0.1.0` → `0.2.0`).
2. Commit, tag `vX.Y.Z`, push.
3. Run `.\packaging\windows\build-installer.ps1` from the NodOne repo.
4. The output is `installer_output\NodOne-Setup-vX.Y.Z.exe`.
5. Compute SHA-256: `Get-FileHash NodOne-Setup-vX.Y.Z.exe -Algorithm SHA256`.
6. In *this* repo:
   - Create a GitHub Release with tag `vX.Y.Z`.
   - Upload the `.exe` as a release asset.
   - Edit `releases.json`: prepend a new entry, update `latest`.
   - Open a PR. CI will validate the schema.
   - Merge to `main`.
7. Within 30 seconds of merge, running NodOne instances see the new version
   via auto-update polling.
