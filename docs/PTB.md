# PTB195
- feat(solarium): add drawer resize functionality with localStorage support
- Add OOBE window style selection for Linux and new preview assets
- Updated to Vue 3.5.21
- Updated various dependencies

# PTB192
- Updated to Vue 3.5.20
- Updated several dependencies
- Added `data-nav-path` attribute to `<NavigationButton>`

# PTB184
- feat: Added "Move to Folder" and "Move to Top" to sidebar playlist context menu
- refactor: Changed playlist sorting behavior, playlist folders are now always at the top while still being sorted
- refactor: Updated create playlist and create playlist folder dialogs

# PTB182
- feat: Scrollers can now be horizontally scrolled by using the scroll wheel while hovering over the buttons
- fix: Readded missing open in new tab
- fix: Fix for exiting mini player causing the WebView2 render freezing up on Windows

# PTB181
- refactor: Improved scrolling for sliders when using the direction buttons
- Fixed missing transition for sweetener Immersive background

# PTB179
- fix: Fixed Sweetener Immersive background when set to "Immersive"
- refactor: Sweetener immersive background now unloads when window is hidden
- refactor: Added Limit Immersive background framerate when not in focus
- refactor: Increased default framerate of Immersive background to better accomidate the increased motion. 30 -> 60 for Immersive mode, 15 -> 25 for Immersive Sweetener
- Updated to Vue 3.5.16

# PTB177
- Compilations / DJ Mix "Albums" will now always display artists even if there is only one

# PTB175
- refactor: Artist picker now uses context menus at mouse position instead of a popup
- refactor: Moved some dialogs to the 3.0 dialog system
- refactor: Transitioning CSelect to use native chromium `<select>` styling

# PTB174
- Readded missing "Pin to Home" in media item context menus

# PTB173
- Updated to Vue 3.5.14
- feat: Improved Artist page artwork color reactivity 
- fix: Fixed artist favorites button not working
- fix: Adjusted RichAlbumGrid offset slightly when album is selected
- refactor: Add to Playlist shortcut now uses correct context menus

# PTB171
- fix: Fixed artist play button not having assigned action
- refactor: removed wait cursor state on context menus
- feat: Add icons to immersive and mini-player options in NowPlayingContextMenu
- refactor: Improve data handling and refresh logic in Browse, ListenNow, and Radio components
- feat: Add artist release date styling and pass artist-release prop to MediaItem components
- refactor: added git branch to build info

# 2.6.1-PTB160
- Performance improvements for pages with a lot of media items

# 2.6.1-PTB153
- fix(albums): fixed portrait album view not rendering
- fix(albums): albums now show key and BPM

# 2.6.1-PTB151
- Replaces current Media Item Artwork component with a newer more flexable version

# 2.6.1-PTB148
- fix(animated-artwork): muted video
  - [because this is a thing apparently](https://music.apple.com/us/playlist/alternative-hip-hop-essentials/pl.c50280b15852442ba25ca9949fa1a6a5)

# 2.6.1-PTB147
- fix(immersive): change how blurmap artwork is acquired, fixed simple artwork not working correctly

# 2.6.1-PTB146
- Fixes an issue where pressing Add to Library in some places could add the item twice

# 2.6.1-PTB141
- New Spatial Presets:
  - Maikiwi ('25 Signature A)
  - Maikiwi ('25 Signature B)
- Updated Editorial Album appearance
  - Fixed incorrect positioning of banner
  - On Calico layout, the top bar colors are now adapted to the editorial banners colors

# 2.6.1-PTB137
- Fixed editorial headers on library albums not appearing
- Improved library albums catalog data

# 2.6.1-PTB134
- Fixes Play and Shuffle buttons on type `library-albums` and `library-playlists` in their respective pages
- Fixed playlist track info proportions. Albums and Artists were too short.

# 2.6.1-PTB131
- Fixes audio normalization

# 2.6.1-PTB125
- Improved data fetching times for Albums and Playlists

# 2.6.1-PTB122
- Implemented search and sorting in new Albums and Playlist pages
- Added disc numbers to albums
  - Discs can be collapsed

# 2.6.1-PTB121
- Split Cider Audio Labs from Cider Audio
  - More Cider Audio Labs presets by Maikiwi are now available from the Marketplace and are updateable independant from Cider itself
  - If you were using a preset that has been moved to the marketplace you will be prompted on startup to download the plugin to restore your previous settings
- Fixed issue where Cider Audio "Atmosphere Realizers" were not localizing properly.
- Fixed an issue where pages on startup would not fully load their content due to an invalid language query
- Marketplace listings are now cached on client

# 2.6.0-PTB117
- Restored UI immersive background settings
- Fixed an issue where playlists would not load correctly from previous PTB

# 2.6.0-PTB112
[Playlists]
- BPM and Key added to playlist tracks (when enabled)

# 2.6.0-PTB107
[Albums]
- Added popularity indicator
- Multiple artists will now show on a track
- More changes to curator notes

# 2.6.0-PTB106
[Playlists + Albums]
- Library Albums now use the new albums page
- Playlist track suggestions that get added now get removed from the suggestion list to allow new suggestions to take their place
- Added unavailable track status
- Playlist tracks now show artists and albums
- Playlist page responsive layout has been improved

# 2.6.0-PTB105
[Playlists + Albums]
- New expanded description "blurb" UI
- Added Apple Digital Master badging to albums
- Added Playlist track suggestions

# 2.6.0-PTB102
- Multiple tracks can now all be removed at once from playlists
- Added Playlist info editor

# 2.6.0-PTB100
- Added Remove from Playlist to playlist tracks
- Fixed switching tracks in playlist not being as quick as it should be

# 2.6.0-PTB99
- Preview of in-development new playlist and album pages
  - Faster loading times
  - Playlist track order can now be modified inline instead of on a different page
  - (Playlists only) Have an option in the menu to revert temporarily to the current playlist page
  - Library Albums currently still use the current page
  - Can be disabled during its preview period under Experimental settings
  - Currently missing a few playlist features, namely sorting.

# 2.6.0-PTB94 / Patch 5
- Fixed issue introduced with track logic update that prevented sorted and filtered playlists from playing in the right order.

# 2.6.0-PTB89
- Fixed notifications for PTB not working

# 2.6.0-PTB88
- Improved track list logic
  - Changing between songs within the same playlist is now much faster
  - Improved handling of large playlists
  - Added warning that it may take more time initially for a large playlist to load

# 2.6.0-PTB86
- Genten specific client settings have been added.
- Fixed some <svg> icons color being stuck to white

# 2.6.0-PTB84
- Resolved an issue that was causing excessive lag in Sing Lyrics
- Added Settings / Advanced / Client Settings
  - Allows easy access to client framework specific settings.
  - Currently only on Windows. macOS and Linux will have support soon.

# 2.5.4-PTB78
- Added recent playlists under "Add to playlist..." in context menus

# 2.5.4-PTB77
- CAP v146
  - Enhances compatibility with planar and non-dynamic headphone drivers (electrostatic headphone users should still leave CAP **disabled**

# 2.5.4-PTB75
- Added new keybind for Miniplayer (default CTRL/Meta + K)

# 2.5.4-PTB74 / 2.5.4 Patch 3
- Fixed card type items having blurry artwork
- Smarter codec selection for animated artwork

# 2.5.4-PTB71
- fix(heroitem): empty items will no longer display

# 2.5.4-PTB70
- fix(compact player): fixed background with HDR enabled

# 2.5.4-PTB65
- Fixed install button not being accessable, preventing updates.

# 2.5.4-PTB64
- The in-app Custom CSS now processes its CSS through the theme system
  - Nested declarations are now supported
  - Automatic `!important` handling
   
# 2.5.4-PTB63
- Updated Editorial Banners
- Updated Marketplace Details Panel

# 2.5.3-PTB59
- Comfy style player now supports the Show Quick Actions option

# 2.5.3-PTB57 / 2.5.3 (Patch 2)
- Fixes an issue where Cider could get stuck and frozen in a loop if "Resume from last page" is enabled and the last page was the OOBE login step

# 2.5.3-PTB54
- Marketplace descriptions now use markdown
- Fix adaptive play-menu button accents and implement functionality for RichAlbumGridItem (#502)
- Refactor DiscordIntegration to clear presence on pause or completion

# 2.5.3-PTB46
- Fixed an issue where drag and drop would not work properly if an item was dragged while it was playing
- flatten settings when searching, individual settings lines will now be shown instead of their entire section

# 2.5.3-PTB44
- Changes to artwork formatting, should result in faster artwork loading.

# 2.5.3-PTB40
- feat(sidebar): sidebar playlist folder opened state will now persist between sessions
- feat(pages): added resume from last session option for startup page
- fix(powerswoosh): fixed play button not working
- fix(updates): fixed channel selection not saving
- refactor(updates): made PTB a top level channel like stable

# 2.5.3-PTB39
- fix(library-songs): fixed some fields being stuck when sorting

# 2.5.3-PTB36
- Revamped Settings UI
  - Searchable
  - Still very much WIP
- fix(search): fixed search suggestion menu
- refactor(NIcon): added [data-icon-name] attribute
- fix(playlist-listings): disregard empty responses

# 2.5.3-PTB35
- Animated Artwork quality is increased at all times and no longer randomly dips down

# 2.5.3-PTB34
- Start of 2.5.3 development period
- Fixes Curator items shelf in Groupings not being visible
- Added support for showing multiple artists artwork in Discord RPC
- Discord RPC now uses iCloud Artwork

# 2.5.2-PTB32
- Up-to-date with stable

# 2.5.2-PTB25 / Prerelease
- Added notification for Plugin and Theme updates on startup
  - Can be disabled under Settings / Extensions
- Added Updates section to the in-app Marketplace

# 2.5.2-PTB24 / Prerelease
- Updated to Vue 3.5.3

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
