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
