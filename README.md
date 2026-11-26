# ChipmunkBoy — Game Boy Game Genie Catalog

This repository hosts the public JSON catalog used by **ChipmunkBoy**, an Android emulator for the original Nintendo Game Boy (DMG).

## Scope

- Platform: **Nintendo Game Boy**.
- Cheat system: **Game Genie only**.
- Accepted code format: **11 hexadecimal characters**, written as `XXX-XXX-XXX`.
- GameShark and Action Replay codes are outside this catalog's scope.
- Short 7-character Game Genie codes must not be added.

## Compatibility and verification

Each catalog entry must identify the exact game release it applies to, including as available:

- Game title;
- region and revision;
- ROM CRC32 (8 hexadecimal characters);
- code and a clear description;
- source URL using HTTPS;
- explicit license or permission allowing redistribution;
- verification status.

Only entries with status `tested` may be offered by the application. ChipmunkBoy additionally requires an **exact CRC32 match** with the loaded ROM before presenting a code as compatible. A matching title, region, or revision alone is not sufficient.

The `tested` status means the code has been tested against the identified ROM release. It must not be assigned based only on a code appearing in another database or website.

## Data and licensing rules

Do not add codes unless their source and redistribution rights have been checked and documented. A source URL by itself is not a redistribution license. Do not copy or import entries from third-party databases unless their license explicitly permits the intended reuse.

An empty catalog is preferable to unverified codes or data with unclear rights.

## JSON catalog

The canonical catalog is [catalog.json](./catalog.json). It uses schema version 1 and is consumed by ChipmunkBoy over HTTPS.

Contributions must preserve the schema and the restrictions above. Please do not add unsupported code formats or claim compatibility without an exact ROM CRC32 and a successful test.
