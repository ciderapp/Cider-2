
Base URL: `http://localhost:10767/`
## Playback API Endpoints Documentation

### `/api/v1/playback`

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
  
- `/queue/move-to-position` - Moves position of queue item to a new position
  - `startIndex` - Index of what queue item to move
  - `destinationIndex` - Index of where to move the queue item
  - `returnQueue`(?) - Returns the queue after the request has finished (slower)

- `/toggle-repeat`
  - Toggles the repeat mode.

- `/toggle-shuffle`
  - Toggles the shuffle mode.

- `/toggle-autoplay`
  - Toggles the autoplay mode.

## Socket.IO Channels

- `API:Playback` - Live Now Playing Feed (readonly)

### `/api/v1/lyrics`

- `/:id` - `:id` - The ID of the item for lyrics.  Library and Catalog types are automatically infered by the endpoint.
  - Returns: Array of lyrics with time codes
