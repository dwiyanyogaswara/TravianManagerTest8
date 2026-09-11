# v4.14.16

## Resource scan validation
- Fixed an undefined `fieldNodes` reference in the scan result payload.
- `fieldNodeCount` now reports the validated unique resource-field count.
- Preserved the ResID + ResGid + Level binding from the same DOM field.
- Preserved the rule that GID is never defaulted to 1.
- Preserved deterministic lowest-level selection and target href normalization.

## Test status
- Source/static scan-path validation completed.
- Real DOM/WebView runtime validation requires an active Travian page/session.
