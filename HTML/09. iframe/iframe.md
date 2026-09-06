# Iframe

# Using the HTML `<iframe>` Element

HTML ka `<iframe>` element use hota hai **ek HTML document ya external content ko current webpage ke andar embed (show)** karne ke liye. Iski help se aap web pages, YouTube videos, Google Maps, PDFs ya kisi aur external content ko apni webpage ke andar ek framed window me display kar sakte ho.

Ye guide `<iframe>` element, uske attributes aur practical examples ko Hinglish me explain karti hai.

## What is an `<iframe>`?

`<iframe>` ka full form **Inline Frame** hai.

Ye HTML tag kisi **external source ka content** current webpage ke andar display karta hai. Iframe ek rectangular area create karta hai jiske andar alag HTML document load hota hai, aur ye content parent webpage se alag (isolated) rehta hai.

### Key Attributes

- **`src`**: Jo URL ya file iframe ke andar dikhani hai uska address specify karta hai.
- **`width`** aur **`height`**: Iframe ki width aur height pixels ya percentage me define karte hain.
- **`name`**: Iframe ko ek naam deta hai taaki links ya scripts us iframe ko target kar sakein.
- **`frameborder`**: Iframe ke border ko control karta hai (`0` = border nahi, `1` = border show hoga).
- **`allow`**: Camera, microphone, fullscreen, autoplay jaise browser features ki permission deta hai.
- **`title`**: Accessibility ke liye iframe ka description provide karta hai.

---

## Example 1: Embedding a Webpage

Aap `src` attribute ki help se poori website ko apni webpage ke andar embed kar sakte ho.

```html
<iframe src="https://www.example.com"
        width="100%"
        height="400"
        title="Example Website">
</iframe>
```

Is code me `https://www.example.com` webpage iframe ke andar load hogi. `width="100%"` iframe ko full width dega aur `height="400"` uski height 400 pixels set karega.

---

## Example 2: Embedding a YouTube Video

YouTube videos ko embed karne ke liye YouTube ka embed URL use kiya jata hai.

```html
<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
</iframe>
```

Ye code YouTube video ko webpage ke andar display karta hai. `allowfullscreen` fullscreen mode enable karta hai aur `allow` attribute video ko autoplay aur picture-in-picture jaise features ki permission deta hai.

---

## Example 3: Using `name` with Links

`name` attribute ki help se hyperlink kisi specific iframe ke andar content load kar sakta hai.

```html
<a href="https://www.example.com" target="myframe">
  Visit Example.com
</a>

<iframe
    name="myframe"
    width="100%"
    height="300"
    title="Targeted Frame">
</iframe>
```

Jab user **Visit Example.com** link par click karega, website new tab me open nahi hogi. Wo `myframe` naam wale iframe ke andar hi load ho jayegi.

---

## Understanding the `allow` Attribute

`allow` attribute iframe ke andar **browser permissions grant** karta hai.

Modern browsers security reasons ki wajah se camera, microphone, fullscreen, autoplay jaise powerful features ko by default block kar dete hain. `allow` attribute ki help se hum iframe ko required permissions dete hain.

### Why do we need it?

Agar sahi `allow` values nahi di gayi, to ye features kaam nahi karenge:

- YouTube autoplay.
- Fullscreen mode.
- Camera aur microphone access.
- Picture-in-Picture mode.

Matlab embedded webpage feature use karna chahegi, lekin browser permission na hone ki wajah se feature block ho jayega.

### How it works

`allow` attribute me permissions semicolon (`;`) se separate likhi jaati hain.

Example:

```html
allow="camera; microphone; fullscreen"
```

Agar kisi specific website ko hi permission deni ho to origin bhi specify kar sakte hain.

```html
allow="camera https://example.com; microphone"
```

Yaha camera permission sirf `example.com` ke liye di gayi hai.

---

## Common `allow` Values

| **Value** | **Kya Allow Karta Hai** | **Kab Use Kare** | **Typical Use Case** |
|------------|---------------------------|------------------|----------------------|
| `autoplay` | Media automatically play ho sakta hai. | Jab video bina click ke start karni ho. | YouTube, Video Players |
| `fullscreen` | Fullscreen mode allow karta hai. | Video ya game fullscreen me dikhana ho. | YouTube, Maps, Games |
| `picture-in-picture` | Floating video window allow karta hai. | Chhoti floating screen me video chalani ho. | YouTube, Video Players |
| `accelerometer` | Device ke accelerometer sensor ka access deta hai. | Motion ya VR experience ke liye. | Games, Interactive Demos |
| `gyroscope` | Device orientation sensor ka access deta hai. | Motion aur AR/VR features ke liye. | Games, AR/VR |
| `clipboard-write` | Clipboard me text copy karne ki permission deta hai. | Copy button ya share widget ke liye. | Code Snippets, Share Widgets |
| `encrypted-media` | DRM protected media play karne deta hai. | Protected streaming content ke liye. | Netflix-style Players, YouTube |
| `camera` | User ke camera ka access deta hai. | Video call ya photo capture ke liye. | Zoom, Google Meet |
| `microphone` | User ke microphone ka access deta hai. | Audio recording ya voice call ke liye. | Speech Recognition, Voice Chat |
| `geolocation` | User ki location access karne deta hai. | Current location dikhane wale maps ke liye. | Google Maps |
| `payment` | Payment Request API use karne deta hai. | Checkout ya payment forms ke liye. | Payment Widgets |
| `usb` | USB devices ka access deta hai. | Hardware interaction ke liye. | USB Device Tools |
| `midi` | MIDI devices ka access deta hai. | Music ya instrument apps ke liye. | Music Production Tools |
| `display-capture` | Screen sharing ya screen capture allow karta hai. | Meeting apps me screen share ke liye. | Google Meet, Zoom |
| `web-share` | Native share dialog open karne deta hai. | Social sharing buttons ke liye. | Share Buttons |

---

## Practical Examples of `allow`

### YouTube-style video (most common)

```html
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen"
  allowfullscreen>
</iframe>
```

Ye YouTube video ko autoplay, fullscreen aur picture-in-picture jaise permissions deta hai.

### Video call / camera + microphone

```html
<iframe
  src="https://meet.example.com"
  allow="camera; microphone; fullscreen"
  width="800"
  height="600"
  title="Video Call">
</iframe>
```

Ye iframe camera, microphone aur fullscreen ki permission ke saath video call webpage embed karta hai.

### Map with location access

```html
<iframe
  src="https://maps.example.com"
  allow="geolocation"
  width="100%"
  height="450"
  title="Interactive Map">
</iframe>
```

Ye iframe Google Map ya kisi map application ko location permission ke saath embed karta hai.

### Minimal permissions (recommended approach)

Sirf wahi permissions do jo iframe ko actual me zarurat ho. Extra permissions dena security ke liye recommended nahi hai.

---

## Example 5: Styling an Iframe

```html
<style>
  .responsive-iframe {
    width: 100%;
    height: 400px;
    border: none;
    margin: 10px;
  }
</style>

<iframe
  src="https://www.example.com"
  class="responsive-iframe"
  title="Styled Frame">
</iframe>
```

Is example me CSS ki help se iframe responsive banaya gaya hai. Width full screen ke according adjust hogi, border remove kiya gaya hai aur margin add ki gayi hai.

---

## Best Practices

- **Accessibility:** Hamesha iframe ke saath `title` attribute zarur add karo taaki screen readers uska purpose samajh sakein.
- **Responsive Design:** Width ko percentage (`100%`) ya CSS se responsive banao.
- **Security:**
  - Untrusted content ke liye `sandbox` attribute use karo.
  - Sirf required permissions hi `allow` me add karo.
  - Sab permissions blindly copy mat karo.
- **Performance:** Ek hi webpage par bahut zyada iframes use mat karo, warna page loading slow ho sakti hai.