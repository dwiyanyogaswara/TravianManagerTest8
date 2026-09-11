# Scan test v4.14.16

Static validation performed for the resource scan path.

Expected invariant per target resource:
- fieldId is 1..18
- gid is 1..4
- level is read from the same field/ancestor chain as fieldId and gid
- no gid fallback/default to 1
- candidates are sorted by level, then fieldId
- target is the first enabled candidate with level < 10
- href is rewritten with the scanned gid and expected village newdid
- database target receives resourceId + resourceGid + minLvl + linkResource from the same lowestResource object

Fix included:
- removed reference to undefined `fieldNodes.length` in the JSON result; fieldNodeCount now uses `uniqueFields`.

Manual runtime test still requires a real Travian page/WebView DOM. Use logs:
`TARGET RES TERENDAH`, `UI FIELD[...]`, and `fieldNodes=...` to verify each village.
