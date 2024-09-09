# 2.5.2-PTB23 / Prerelease
- refactor(remote-connect): add app store links
- Updated remote connection UI

# 2.5.2-PTB22
- refactor(applemusic): fix missing volume percentage in miniplayer

# 2.5.2-PTB21
- Added Tweaks / Lyrics / Line Staggering
- Added Tweaks / Lyrics / Line Staggering (Immersive)

# 2.5.2-PTB19
- Improved lyric scrolling appearance
- Added Publish in profile and search checkbox to editable playlists
- Under the hood fixes for content loading
- Fixed Third Party Lyrics appearing when disabled

# 2.5.2-PTB18
- Fixed `/api/v1/playback/queue/remove-by-index` not working properly

# 2.5.2-PTB17
- Added Enable Static Lyrics under Visual / Lyrics
- Fixes issue where home page content may fail to load

# 2.5.2-PTB16
- feat(rpc): added more RPC commands

POST `/api/v1/playback/queue/remove-by-index` - Takes `index` in body

POST `/api/v1/playback/queue/clear-queue`

GET `/api/v1/playback/shuffle-mode` - Returns status as data.value

GET `/api/v1/playback/repeat-mode` - Returns status as data.value

GET `/api/v1/playback/autoplay` - Returns status as data.value

GET `/api/v1/playback/library-status` - Returns up to date library status and rating for current track

# 2.5.2-PTB15
- Updated to Vue 3.5.0

# 2.5.2-PTB14
- chore: fix play later (shift+z) (Command Palette)
- feat(applemusic): Add Fyre immersive sing parameters CSS
- refactor(applemusic): Update immersive sing options and layout
- Update the title of the sing options modal to "Focus Mode Settings" for clarity.
- Refactor the ImmersiveLayout component to improve code organization and readability.
- Rename the "Sing Along" button to "Focus Mode" to better reflect its purpose.
- refactor(wsapi): Update serverRunning and serverPort variables
- Update the serverRunning and serverPort variables in the WSAPI module.
- refactor(musickit): Update interact function and add bandaid fix
- chore(utils): Update setFavorite function and add bandaid fix

# 2.5.2-PTB13
- feat(rpc): added several RPC commands
- `/api/v1/playback/play-url` - Takes a `url` in body and will immediately play the item or track associated with the URL
- `/api/v1/playback//play-item-href` - Similar to play-url but takes an API href instead
- `/api/v1/playback/play-later`, `/play-next`, `/play-item` - Takes `id`  and `type
- `/api/v1/playback//queue/change-to-index` - Jumps to and plays the index requested.  Takes `index` (number) in body

# 2.5.2-PTB12
- Fixed `/api/v1/playback/queue` not working on macOS / Linux

# 2.5.2-PTB11
- refactor(device): Exclude unwanted and VPN network interfaces
- refactor(connectivity): Add IP check and revise wording.
- refactor(device): exclude unwanted network interfaces

# 2.5.2-PTB10
- feat(rest-api): added /v1/lyrics/:id, automatically infers library or catalog based on ID
- feat(rpc): added queue move-to-position
- `/api/v1/playback/queue` now properly returns the queue

# 2.5.2-PTB9
- Unused code cleanup
- feat(connectivity): add Cider Remote Testflight link for electron and dotnet frameworks

# 2.5.2-PTB7
- Fixed issue where Socket.IO API was not emitting playback events on macOS or Linux

# 2.5.2-PTB6
- Fixes Discord RPC option being grayed out on OOBE for Windows
- WSAPI `playbackStatus.nowPlayingStatusDidChange` is now called when library status changes
- Added Remote Device pairing QR code in External Apps section
- feat(api): added external messages API, allows for messages to be sent over the rest api for code on the client to listen to (one-way)
  - `POST` `/api/v1/messages/message`
  - Takes a `type` which is the name of the listener
  - The `data` property is what gets sent
- feat(themes): added `[theme-hint-uses-artwork-color]` to help with identifying elements that use artwork color
- Added body[app-mode] with possible modes being: `browser`, `miniplayer`, `immersive`
- Window can now be dragged from empty sidebar region on macOS when using Calico or Montara

# 2.5.2-PTB4-5
- automatic language setting
- fix(updates): fixed an issue where PTB branch would not notify for updates

# 2.5.2-PTB3
- Added i18n strings for Marketplace
- Added "Submit Your Theme/Plugin" button to navigation

# 2.5.2-PTB2
- Added PTB warning
- Added PTB changelog link in Main Menu -> Help -> PTB Changelog

# 2.5.2-PTB1

- fix(immersive): navigation always opens browser
- refactor(musickit): adjust isInLibrary API request and add personalRating field
- fix(themes): Fixed typo with ImmersiveCoverflowPlayer SFC name
- fix(mediaitem-properties): removed broken glass effect
- refactor(applemusic): adjust padding in ImmersiveDrawerContent.vue
- feat(plugins): expose listitemprovider
- fix(dotnet): double click to maximize on windows
