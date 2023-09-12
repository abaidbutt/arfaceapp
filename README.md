# Web AR Face Filter app  
    
## Requirements

- [client token](#obtaining-banuba-client-token)
- [Nodejs](https://nodejs.org/en/) installed
- Browser with support of [WebGL 2.0](https://caniuse.com/#feat=webgl2)



### Obtaining Client token

A  Client token is required to get Banuba SDK Web AR working.

To receive a new **trial** client token please fill in the [form on banuba.com](https://www.banuba.com/face-filters-sdk) website, or contact us via [abaidbutt](mailto:bestabaidullahbutt@gmail.com).

## Environment setup and local run

Clone the repository

```sh
git clone https://abaidbutt/arfaceapp.git
```

Insert Tokeen [client token](#obtaining-banuba-client-token) into `ClientToken.js`

```js
window.CLIENT_TOKEN = "PUT YOUR CLIENT TOKEN HERE"
```

Run the live server in the cloned folder
```sh
npx live-server
```

Open [localhost:8080](http://localhost:8080)

## Adding a new effect

Zip the effect folder and put it under the `effects/` subfolder
```diff
quickstart-web/
   effects/
     BackgroundPicture.zip
     BackgroundBeauty.zip
     BigPinkGlasses.zip
     glasses_Banuba.zip
     Hipster3.zip
+    NewEffect.zip
     Hair_recoloring.zip
   BanubaClientToken.js
   index.html
   README.md
   styles.css
```

Add the effect name into `effects` array at [index.html, line 65](/index.html#L65)

```diff
<script type="module">
  import { Effect, Webcam, Player, VideoRecorder, ImageCapture, Dom } from "https://cdn.jsdelivr.net/npm/@banuba/webar/dist/BanubaSDK.browser.esm.min.js"

  const effects = [
+   "NewEffect",
    "BackgroundPicture",
    "BackgroundBeauty",
    "BigPinkGlasses",
    "glasses_Banuba",
    "Hipster3",
    "Hair_recoloring"
  ]
```


