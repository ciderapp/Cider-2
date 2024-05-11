## This document is still a work in progress

- `.lyric-line-container --lyric-duration-completion-multi`: A floating point value of 0-1 that represents the completion of the current lyric line
- `.lyric-line-container --height`: Current height of the lyric line container
- `.lyric-line-container --lyric-duration`: Duration of the current lyric line in CSS seconds
- `.lyric-line-container --lyric-duration-completion-rate`: Duration of the current lyric line as a CSS % value
- `.lyric-line-container --util-mod-2`: A CSS variable that alternates between -1 and 1 every alternating line
- `.lyric-line-container.has-multiple-lyrics`: Added to the lyric line container when multiple lines are visible
- `.lyric-line-container.position-0`: The first lyric line when multiple lines are visible
- `.lyric-line-container.position-1`: The second lyric line when multiple lines are visible
- `.lyric-line-container.position-2`: The third lyric line when multiple lines are visible
- `.lyric-line-container.position-3`: The fourth lyric line when multiple lines are visible
- `.lyric-line-container[util-lyric-index=LYRIC_INDEX]`: The index of the current lyric line
- `.lyric-line-container[util-mod-2]`: Appled when the current lyric line is an even number
- `.lyric-line.second-vocalist`: This lyric line is a second vocalist line

- `.lyric-line.active`: This lyric line is an active line
- `.lyric-line.collapsable`: This lyric line can be collapsed
- `.lyric-line.has-syllables`: This lyric line is per-syllable aka Sing lyrics
- `.lyric-line.lyric-background-vocal`: This lyric line is a background vocal line
- `.lyric-line.finished`: This lyric line is finished but still visible

- `.lyric-word.active`: This lyric word is an active word
- `.lyric-word.backgrond-vocal`: This lyric word is a background vocal word
- `.lyric-word.current-word`: This lyric word is the current word
- `.lyric-word.glowy-text`: This lyric word has a glow effect
- `.lyric-word.finished-word`: This lyric word is finished but still visible
- `.lyric-word --word-duration`: Word duration in CSS seconds
- `.lyric-word --word-duration-raw`: Word duration clamped between wordDuration \* 2, 1, 1.1. Used in wave effect
- `.lyric-word --word-intensity`: Word duration clamped between wordDuration \* 100,0,100. Used to create subtle glow effect on all words
- `.lyric-word --char-count`: Number of characters in the word
