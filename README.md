# YouTube-music-video-5M

by Keunwoo Choi

## Statistics

  * 5119955 video ID's in youtube in 20 text files.
  * file name: `"youtube_video_ids_{:0d}_{}.txt".format(file_index, n_ids_this_file)`
  * Entries of the files are either
    - `"\n"`
    - `"# new artist:\t{}\t{}\n".format(artist_name, artist_spotify_id)`
    - `"{}\n".format(youtube_video_id)` 
  * E.g., the first 10 lines of `youtube_video_ids_00_206947.txt` is...
```

# new artist: Drake 3TVXtAsR1Inumwj472S9r4

3t195yz9xCc
VkXjvHfP3MM
7LnBvuzjpr4
1Ldzm7KGECI
HL1UzIK-flA
3XR5mhXtpXw
WsPfSXJaelk

```

  * Files and entries are sorted by some sort of artist popularity.
  * Each text file includee video ID's of 500 artists
  * overall, they are from approximately 10K artists.

## Crawlling by how?
  * Using YouTube search API with keywords of `"{} official music video".format(artist_name)`. Hopefully it's more official music videos with a professional quality rather than amateur videos.

## Utilities
  * [pytube](https://github.com/nficano/pytube)
