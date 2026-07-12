[CENTER][SIZE=7][B]FlyPlugin[/B][/SIZE]
[SIZE=4]Simple Pay-As-You-Fly Economy Flight for Paper 26.2[/SIZE][/CENTER]

[COLOR=#ff4d4d][B]Language notice:[/B][/COLOR] The SpigotMC resource page, documentation and support channel are English-only. Chinese-language support is not provided on SpigotMC.

The plugin's in-game messages and default configuration comments are currently written in Chinese.

[SIZE=5][B]About FlyPlugin[/B][/SIZE]

FlyPlugin is a lightweight economy-based flight plugin for Paper 26.2. A player pays the configured amount when flight starts and is charged again every 60 seconds while the paid flight session remains active. Vault connects FlyPlugin to the server's economy provider.

The plugin is intentionally focused on a small workflow: start paid flight, continue periodic billing, stop flight manually, or stop it automatically when the balance is insufficient or the player disconnects.

[SIZE=5][B]Compatibility[/B][/SIZE]

[LIST]
[*][B]Server software:[/B] Paper 26.2 only
[*][B]Java:[/B] 25 or newer
[*][B]Required dependency:[/B] Vault
[*][B]Required service:[/B] A Vault-compatible economy plugin
[*][B]Plugin version:[/B] 1.1.2
[*][B]Build API:[/B] Paper API 26.2.build.56-alpha
[*]Spigot and Paper versions other than 26.2 have not been tested for this release and are not claimed as supported
[/LIST]

[SIZE=5][B]Free Resource[/B][/SIZE]

FlyPlugin should be published as a [B]free resource[/B] with a price of [B]0.00[/B]. It is a small, single-purpose, open-source plugin released under the MIT License, with no paid service, premium integration or gated feature set. Its current permission and configuration limits also make a free listing more appropriate than a paid resource.

[SIZE=5][B]Main Features[/B][/SIZE]

[LIST]
[*]Start paid flight with one player command
[*]Immediate first charge when a flight session starts
[*]Automatic repeated charge every 60 seconds
[*]Automatic flight shutdown when the player cannot afford the next charge
[*]Manual flight shutdown
[*]Disconnect cleanup and flight-state reset on the next join
[*]Configurable price and console transaction logging
[*]Configuration reload command
[*]No database or external storage service
[/LIST]

[SIZE=5][B]Economy Transaction Flow[/B][/SIZE]

When a player runs [B]/flystart[/B], FlyPlugin checks whether the Vault economy reports a sufficient balance, requests the first withdrawal, enables flight and starts a repeating billing task. Every 60 seconds, it checks the balance again and requests another withdrawal. If the balance is insufficient, paid flight is disabled.

Charges are prepaid for each period. Stopping early does not produce a partial refund. FlyPlugin relies on the configured Vault economy provider and does not bundle an economy implementation.

[SIZE=5][B]Flight State and Data[/B][/SIZE]

Active billing tasks and pending join resets are stored in memory only. FlyPlugin does not create a player-data database or save balances itself. Economy balances remain the responsibility of the Vault economy provider. When a player disconnects during paid flight, the billing task is cancelled and the plugin resets flight permission when that player next joins.

[SIZE=5][B]Security and Permissions[/B][/SIZE]

Version 1.1.2 does not declare or check permission nodes. This means [B]/flystart[/B], [B]/flystop[/B] and [B]/flyreload[/B] are not protected by built-in permissions. Server owners should restrict commands externally if necessary, especially [B]/flyreload[/B]. This limitation is disclosed here and in the full documentation.

[SIZE=5][B]Dependencies[/B][/SIZE]

[LIST]
[*][URL=https://www.spigotmc.org/resources/vault.34315/]Vault[/URL] is required and is not bundled
[*]A separate Vault-compatible economy plugin is required and is not bundled
[*]Paper API and Vault API are compile-time provided dependencies and are not shaded into the release jar
[/LIST]

[SIZE=5][B]Links[/B][/SIZE]

[LIST]
[*][URL=https://github.com/yangzijian52/FlyPlugin]Source Code[/URL]
[*][URL=https://github.com/yangzijian52/FlyPlugin/releases]GitHub Releases[/URL]
[*][URL=https://github.com/yangzijian52/FlyPlugin/issues]Bug Reports and English Support[/URL]
[*][URL=https://github.com/yangzijian52/FlyPlugin/blob/main/LICENSE]MIT License[/URL]
[/LIST]

[SIZE=5][B]Important Notes[/B][/SIZE]

[LIST]
[*]The actual billing interval in version 1.1.2 is fixed at 60 seconds. The [B]charge-interval[/B] configuration value is currently not applied.
[*]The [B]auto-save-interval[/B] configuration value is currently unused because FlyPlugin stores no plugin-owned persistent player data.
[*]Existing active sessions keep the price captured when flight started, even after a configuration reload. Restart the session to use the new price.
[*]Stopping paid flight sets the player's flight permission to false. Test interaction with creative mode or other flight-management plugins before production use.
[*]Version 1.1.2 has no automated test suite. The release is compile-verified; no new live-server test was performed for this documentation update.
[/LIST]
