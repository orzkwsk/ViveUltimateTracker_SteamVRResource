# VIVE Ultimate Tracker display resources

SteamVR/OpenVR resource-only package for use as a Git submodule. Its public
namespace is `vut_display_resources`.

Register the directory containing `driver.vrdrivermanifest` with SteamVR using
`vrpathreg adddriver "<package-directory>"`. Keep this package in its own directory.
Its manifest uses that directory as its root, so it remains independent of any
other installed driver. Applications publish the optional descriptor from
`display-resources.json` through a compatible public protocol.

## Contents

- `resources/rendermodels/vive_ultimate_tracker/`: component JSON, OBJ, MTL and
  diffuse texture. Geometry, material, texture and model-local transforms are
  preserved. The unavailable optional thumbnail reference is omitted.
- `resources/icons/`: eight original 32px PNG/GIF status icons, preserved.
  `DeviceStandbyAlert` explicitly reuses the existing standby icon so waiting
  does not select the output adapter's generic default for that slot.
- `resources/driver.vrresources`: original status mapping with this package's
  namespace substituted and the standby-alert slot assigned to the standby icon.
- `sources/asset-origins.json`: source-relative names and content hashes.

After replacing assets, use new references or restart the output Provider
according to its resource-cache rules. See `NOTICE.md` for asset provenance
and licensing information.
