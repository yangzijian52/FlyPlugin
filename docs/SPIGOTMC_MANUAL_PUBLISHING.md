# FlyPlugin SpigotMC Manual Publishing Guide

## Release Details

- **Resource type:** Free
- **Price:** `0.00`
- **Reason:** FlyPlugin is a small, single-purpose, open-source MIT plugin with no premium service or gated feature set. Version 1.1.2 also has disclosed command-permission and configuration limitations, so a paid listing is not appropriate.
- **License:** MIT License
- **Upload file:** `target/FlyPlugin-1.1.2.jar`
- **GitHub release:** https://github.com/yangzijian52/FlyPlugin/releases/tag/1.1.2
- **Source code:** https://github.com/yangzijian52/FlyPlugin
- **Resource-page BBCode:** `docs/SPIGOTMC-RESOURCE.md`
- **Full-documentation BBCode:** `docs/SPIGOTMC-RESOURCE-BBCODE.txt`

## Suggested SpigotMC Fields

- **Title:** `FlyPlugin`
- **Tag line:** `Simple pay-as-you-fly economy flight for Paper 26.2`
- **Category:** Economy
- **Resource type:** Free resource
- **Price:** `0.00`
- **Version:** `1.1.2`
- **Tested server version:** `Paper 26.2`
- **Java requirement:** `Java 25+`
- **Required dependencies:** `Vault and a Vault-compatible economy plugin`
- **Source URL:** `https://github.com/yangzijian52/FlyPlugin`
- **Support URL:** `https://github.com/yangzijian52/FlyPlugin/issues`
- **License:** `MIT`
- **External download:** Do not use one if direct jar upload is available.

## Important Warnings

- The SpigotMC resource page, documentation and support channel are English-only. Chinese-language support is not provided on SpigotMC.
- Runtime messages and default configuration comments are currently Chinese.
- Claim support only for Paper 26.2 with Java 25 or newer. Do not claim Spigot compatibility.
- Vault and a Vault-compatible economy provider are both required and are not bundled.
- Version 1.1.2 has no built-in permission checks or command aliases. In particular, `/flyreload` is not administrator-protected.
- Billing is fixed at 1,200 ticks. The `charge-interval` configuration value is present but ignored.
- `auto-save-interval` is unused because the plugin has no persistent player-data file.
- Existing paid-flight sessions retain the price captured when they started after `/flyreload`.
- Stopping flight forces the player's flight permission off and may conflict with creative mode or other flight plugins.
- The artifact is compile/package verified. No automated tests exist, and no new live-server test was performed for this documentation-only update.

## Manual Publish Steps

1. Sign in to SpigotMC and start creating a new resource.
2. Select a free resource and set the price to `0.00` if the form displays a price field.
3. Enter the suggested title, tag line, category, version, compatibility, dependency and license fields above.
4. Upload `target/FlyPlugin-1.1.2.jar` directly.
5. Paste the complete contents of `docs/SPIGOTMC-RESOURCE.md` into the resource description field.
6. Paste `docs/SPIGOTMC-RESOURCE-BBCODE.txt` into the documentation page or additional documentation area. If the current SpigotMC form provides only one description field, append it after the resource-page BBCode.
7. Add the GitHub source, release and issue links.
8. Preview the BBCode and verify that headings, lists, links, colors and code blocks render correctly.
9. Confirm the English-only support statement and all limitations remain visible before submission.
10. Verify the uploaded jar filename, version and download once from the draft/preview page if SpigotMC permits it.
11. Submit the resource manually and complete any SpigotMC moderation questions.
12. After publication, add the final SpigotMC resource URL to the GitHub README in a separate documentation commit.
