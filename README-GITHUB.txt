FongMi Safe - GitHub deployment

1. Create a GitHub repository, e.g. fongmi-safe.
2. Upload this package preserving v1/ and v2/.
3. Commit.
4. Copy the exact 40-character commit SHA.
5. First test v1/config.json using its raw.githubusercontent.com URL at that commit.
6. For V2, replace USER, REPO and COMMIT in v2/config-template.json with your values and commit the edit.
7. Point FongMi to the raw config URL at the new exact commit SHA.
8. Never use main/master in the final URLs.

V1 has no JS/JAR/Python and is the recommended baseline.
V2 adds the exact frozen drpy2, drpy-core-lite and LIBVIO files.

Important: drpy2 imports ./drpy-core-lite.min.js. Remote relative-module resolution must be tested on your installed FongMi build. If V1 works but LIBVIO fails, do not grant storage permission as a workaround.

Keep Android shared-storage/All files access and Install unknown apps disabled when HTTPS loading works.
