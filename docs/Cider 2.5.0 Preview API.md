
Base URL: `http://localhost:10767/`
# Playback API Endpoints Documentation

## `/api/v1/playback`

### GET Endpoints

- `/active`
  - Returns the active status.

- `/is-playing`
  - Checks if a track is currently playing.
  - Returns: `{ is_playing: boolean }`

- `/now-playing`
  - Retrieves information about the currently playing track.
  - Returns: `{ info: object }`

- `/queue`
  - Gets the current queue.

- `/shuffle-mode`
  - Gets the current shuffle state.

- `/repeat-mode`
  - Gets the current repeat state.

- `/api/v1/playback/autoplay`
  - Gets autoplay state
 
- `/api/v1/playback/library-status`
  - Returns favorite and library added states

- `/volume`
  - Gets the current volume level.
  - Returns: `{ volume: string }`

### POST Endpoints

- `/play`
  - Plays the current track.

- `/pause`
  - Pauses the current track.

- `/playpause`
  - Toggles between play and pause.

- `/stop`
  - Stops the current track.

- `/next`
  - Skips to the next track.

- `/previous`
  - Goes back to the previous track.

- `/seek`
  - Seeks to a specific position in the current track.
  - Requires: `{ position: number }`

- `/volume`
  - Sets the volume level.
  - Requires: `{ volume: number }`

- `/add-to-library`
  - Adds the current song to the library.

- `/set-rating`
  - Sets the rating for the current track.
  - Requires: `{ rating: number }` (-1, 0, 1)

- `/play-url`
  - Takes a `url` in body and will immediately play the item or track associated with the URL

- `/play-item-href`
  - Takes a `href` in body and will immediately play the item or track associated with the API href
 
- `/play-later`
  - Takes `id` and `type`

 - `/play-next`
  - Takes `id` and `type`

 - `/play-itemr`
  - Takes `id` and `type`
 
- `/queue/move-to-position` - Moves position of queue item to a new position
  - `startIndex` - Index of what queue item to move
  - `destinationIndex` - Index of where to move the queue item
  - `returnQueue`(?) - Returns the queue after the request has finished (slower)

- `/queue/change-to-index` - Jumps to and plays the index requested. Takes `index` (number) in body

- `/queue/remove-by-index` - Removes queue item by index. Takes `index` (number) in body
- 
- `/queue/clear-queue` - Clears the queue

- `/toggle-repeat`
  - Toggles the repeat mode.

- `/toggle-shuffle`
  - Toggles the shuffle mode.

- `/toggle-autoplay`
  - Toggles the autoplay mode.

## Socket.IO Channels

- `API:Playback` - Live Now Playing Feed (readonly)

# Lyrics API

## `/api/v1/lyrics`

- `/:id` - `:id` - The ID of the item for lyrics.  Library and Catalog types are automatically infered by the endpoint.
  - Returns: Array of lyrics with time codes

# Messaging

## `/api/v1/messages`

### POST
- `/message`
  - `type` - Name of the listener, defined either in docs or by a plugin.
  - `data` - Data to be sent.
 
# Apple Music API

## `/api/v1/amapi`

### POST
- `/run-v3`
  - `path` (string)

- `/run-v3turbo`
  - `path` (string)
