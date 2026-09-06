# Using Audio and Video Media in HTML

Ye guide HTML me **Audio** aur **Video** elements ko use karna explain karti hai. Audio aur Video tags ki help se hum website me songs, podcasts, sound effects, tutorials aur videos embed kar sakte hain.

Har section me definition, attributes, examples aur practical scenarios diye gaye hain.

---

# Audio

## Definition

`<audio>` tag ka use webpage me **sound content** embed karne ke liye hota hai. Isse MP3, WAV aur OGG format ki audio files play ki ja sakti hain.

Ek `<audio>` tag ke andar multiple `<source>` elements use kiye ja sakte hain taaki different browsers compatible audio format choose kar saken.

---

## Attributes

- **`src`** → Audio file ka path ya URL specify karta hai.
- **`controls`** → Browser ke default audio controls (Play, Pause, Volume) show karta hai.
- **`autoplay`** → Page load hote hi audio automatically play karta hai.
- **`loop`** → Audio ko continuously repeat karta hai.
- **`muted`** → Audio ko by default mute rakhta hai.

---

## Examples

### `src`

Audio file directly `src` attribute se specify ki ja sakti hai.

```html
<audio src="podcast-episode.mp3">
  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Ye `podcast-episode.mp3` audio file ko load karta hai.

---

### `controls`

Audio controls display karta hai.

```html
<audio controls>
  <source src="background-score.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Play, Pause aur Volume controls browser automatically show karega.

---

### `autoplay`

Page load hote hi audio automatically play hoti hai.

```html
<audio autoplay muted>
  <source src="welcome-sound.ogg" type="audio/ogg">
  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Modern browsers me autoplay ke saath `muted` use karna zaruri hota hai.

---

### `loop`

Audio ko baar-baar repeat karta hai.

```html
<audio controls loop>
  <source src="ambient-loop.wav" type="audio/wav">
  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Audio end hone ke baad fir se start ho jayegi.

---

### `muted`

Audio by default mute hoti hai.

```html
<audio controls muted>
  <source src="intro-music.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Audio play hogi lekin sound mute rahega.

---

# Video

## Definition

`<video>` tag ka use webpage me **video content** embed karne ke liye hota hai.

Ye MP4, WebM aur OGG video formats support karta hai. Multiple `<source>` elements use karke browser compatibility improve ki ja sakti hai.

`<track>` element subtitles aur captions add karne ke liye use hota hai.

---

## Attributes

- **`src`** → Video file ka path ya URL specify karta hai.
- **`controls`** → Browser ke default video controls show karta hai.
- **`autoplay`** → Video automatically play karta hai.
- **`loop`** → Video continuously repeat hoti hai.
- **`muted`** → Video ka sound mute rakhta hai.
- **`poster`** → Video play hone se pehle preview image show karta hai.
- **`width`** → Video ki width set karta hai.
- **`height`** → Video ki height set karta hai.
- **`playsinline`** → Mobile devices me fullscreen ke bajaye inline video play karta hai.
- **`disablePictureInPicture`** → Picture-in-Picture option disable karta hai.

---

## Examples

### `src`

Video file directly `src` attribute se specify ki ja sakti hai.

```html
<video src="intro-video.mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Ye `intro-video.mp4` video load karta hai.

---

### `controls`

Video controls show karta hai.

```html
<video controls>
  <source src="tutorial-video.webm" type="video/webm">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Play, Pause, Volume aur Fullscreen controls show honge.

---

### `autoplay`

Video automatically play hoti hai.

```html
<video autoplay muted>
  <source src="splash-video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Autoplay ke saath `muted` use karna recommended hai.

---

### `loop`

Video continuously repeat hoti hai.

```html
<video controls loop>
  <source src="background-video.webm" type="video/webm">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video khatam hone ke baad fir se play hogi.

---

### `muted`

Video mute hoti hai.

```html
<video controls muted>
  <source src="silent-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video ka sound mute rahega.

---

### `poster`

Video start hone se pehle preview image show hoti hai.

```html
<video controls poster="video-preview.jpg">
  <source src="product-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Poster image thumbnail ki tarah display hoti hai.

---

### `width`

Video ki width set karta hai.

```html
<video controls width="800">
  <source src="conference-talk.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video ki width 800 pixels hogi.

---

### `height`

Video ki height set karta hai.

```html
<video controls height="450">
  <source src="animation-clip.webm" type="video/webm">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video ki height 450 pixels hogi.

---

### `playsinline`

Mobile devices me video fullscreen ke bajaye page ke andar play hoti hai.

```html
<video controls playsinline>
  <source src="mobile-friendly-video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Ye mobile users ke liye better experience deta hai.

---

### `disablePictureInPicture`

Picture-in-Picture mode disable karta hai.

```html
<video controls disablePictureInPicture>
  <source src="locked-video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

User video ko floating window me open nahi kar sakta.

---

# Responsive Video

## Definition

Responsive video har screen size par automatically adjust ho jati hai.

---

## Example

```html
<video controls width="100%" style="max-width:900px;">
  <source src="responsive-video.mp4" type="video/mp4">
  <source src="responsive-video.webm" type="video/webm">

  <track src="subtitles.vtt"
         kind="subtitles"
         srclang="en"
         label="English">

  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

- Video full width leti hai.
- `max-width` se desktop par maximum size limit hoti hai.
- `<track>` subtitles add karta hai.

---

# Scenarios and Examples

Ye real-life scenarios hain jahan audio aur video use hote hain.

---

## Scenario 1: Background Music for a Website

**Use Case:** Portfolio website me background music continuously play karna.

```html
<audio autoplay muted loop>
  <source src="ambient-background.mp3" type="audio/mpeg">
  <source src="ambient-background.ogg" type="audio/ogg">

  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Background music autoplay, mute aur loop mode me chalegi.

---

## Scenario 2: Podcast Player

**Use Case:** Blog page me podcast episode play karna.

```html
<audio controls preload="metadata">
  <source src="podcast-episode-101.mp3" type="audio/mpeg">
  <source src="podcast-episode-101.ogg" type="audio/ogg">

  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Podcast player me controls available honge aur metadata pehle load hoga.

---

## Scenario 3: Instructional Video Tutorial

**Use Case:** E-learning website me tutorial video aur subtitles.

```html
<video controls
       width="640"
       height="360"
       poster="tutorial-preview.jpg">

  <source src="coding-tutorial.mp4" type="video/mp4">
  <source src="coding-tutorial.webm" type="video/webm">

  <track src="tutorial-subtitles.vtt"
         kind="subtitles"
         srclang="en"
         label="English">

  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video ke saath poster image aur subtitles available hain.

---

## Scenario 4: Mobile-Friendly Video Ad

**Use Case:** Mobile users ke liye promotional video.

```html
<video controls
       playsinline
       width="100%"
       style="max-width:800px;">

  <source src="product-ad.mp4" type="video/mp4">
  <source src="product-ad.webm" type="video/webm">

  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video mobile par fullscreen ke bajaye inline play hogi.

---

## Scenario 5: Synchronized Audio and Video Narration

**Use Case:** Documentary video ke saath separate narration audio.

```html
<video controls mediagroup="doc-sync" width="600">
  <source src="documentary-clip.mp4" type="video/mp4">

  Your browser does not support the video tag.
</video>

<audio controls mediagroup="doc-sync">
  <source src="narration-track.mp3" type="audio/mpeg">

  Your browser does not support the audio element.
</audio>
```

**Explanation (Hinglish):**

Audio aur video same media group me synchronize kiye gaye hain.

---

## Scenario 6: Streaming Media from a CDN

**Use Case:** Live event video CDN se stream karna.

```html
<video controls
       crossorigin="anonymous"
       preload="metadata"
       width="800">

  <source src="https://cdn.example.com/live-event.webm" type="video/webm">
  <source src="https://cdn.example.com/live-event.mp4" type="video/mp4">

  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Video CDN se securely load hoti hai aur metadata pehle load hota hai.

---

## Scenario 7: Locked Video Player

**Use Case:** Educational platform me Picture-in-Picture disable karna.

```html
<video controls
       disablePictureInPicture
       width="700"
       height="400">

  <source src="lecture-video.mp4" type="video/mp4">

  <track src="lecture-captions.vtt"
         kind="captions"
         srclang="en"
         label="English">

  Your browser does not support the video tag.
</video>
```

**Explanation (Hinglish):**

Students sirf webpage ke andar hi video dekh sakte hain.

---

# Best Practices

- **Accessibility:** Videos ke saath `<track>` use karke subtitles ya captions zarur add karo.
- **Compatibility:** Multiple `<source>` formats use karo (MP4 + WebM, MP3 + OGG).
- **Performance:** `preload="metadata"` ya `preload="none"` use karke loading optimize karo.
- **Compression:** Media files compress karo taaki website fast load ho.
- **Responsive Design:** `width="100%"` aur `max-width` use karke responsive videos banao.
- **Testing:** Chrome, Firefox, Safari aur mobile devices par media playback test karo.
- **User Experience:** `autoplay` bina `muted` use mat karo aur `poster` image use karke video preview dikhao.

---

# Summary

HTML me Audio aur Video tags multimedia content embed karne ke liye use hote hain.

| **Element / Attribute** | **Use (Hinglish)** |
|--------------------------|---------------------|
| `<audio>` | Music, podcast aur sound effects play karne ke liye. |
| `<video>` | Video content embed karne ke liye. |
| `controls` | Play, Pause, Volume controls show karta hai. |
| `autoplay` | Page load hote hi media automatically play karta hai. |
| `loop` | Media ko continuously repeat karta hai. |
| `muted` | Media ko by default mute rakhta hai. |
| `poster` | Video start hone se pehle preview image dikhata hai. |
| `playsinline` | Mobile par inline video playback allow karta hai. |
| `disablePictureInPicture` | Picture-in-Picture mode disable karta hai. |
| `<track>` | Video me subtitles aur captions add karta hai. |

Audio aur Video elements ka sahi use website ko interactive, accessible aur user-friendly banata hai.