# berikesan media

Static media (videos, photos) for berikesan invitations, served by GitHub Pages at
https://media.berikesan.com.

One folder per client, named after the invitation slug:

```
wiwin-angga/
  bg.mp4        background video
  bg.jpg        poster shown until the video plays
```

Video guidelines for backgrounds: 720p H.264 MP4, 10-20 s loop, 2-5 MB, no audio.

```
ffmpeg -i input.mp4 -vf "scale=-2:1280" -c:v libx264 -crf 28 -preset slow -an -movflags +faststart bg.mp4
```

The invitation code references files by URL, e.g.
`https://media.berikesan.com/wiwin-angga/bg.mp4` (set in the client's `content.ts`).

Files deleted here stay in git history, so do not upload anything the client wants kept private.
