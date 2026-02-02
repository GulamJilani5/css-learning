⏺️ ➡️ 🟦 🔵 🟢 🔴 ⭕ 🟠 🟣 🟥 🟧 ✔️ ☑️ • ‣ → ⁕

# ⏺️ HTML5 API

- HTML5 APIs are built-in browser APIs that allow web applications to do things that earlier needed plugins (Flash, Java applets, etc.).
- They give JavaScript superpowers to:
  - Access device features
  - Store data locally
  - Work offline
  - Handle media
  - Improve performance & UX

## ➡️ Web Storage API

- Stores data inside the browser.
  | Storage | Capacity | Lifetime |
  | ---------------- | -------- | ----------- |
  | `localStorage` | ~5–10 MB | Permanent |
  | `sessionStorage` | ~5 MB | Tab session |

```js
localStorage.setItem("token", "abc123");
localStorage.getItem("token");
```

- Used in auth tokens, themes, preferences

## ➡️ Geolocation API

- Gets the user’s location (with permission)

```js
navigator.geolocation.getCurrentPosition((pos) => {
  console.log(pos.coords.latitude, pos.coords.longitude);
});
```

- Used in maps, delivery apps, ride-hailing apps

## ➡️ WebSocket API

- Enables real-time communication.

```js
const socket = new WebSocket("ws://localhost:8080");
socket.onmessage = (event) => console.log(event.data);
```

- Used in chat apps, stock prices, live tracking

## ➡️ Web Workers API

- Runs JavaScript in background threads.

```js
const worker = new Worker("worker.js");
worker.postMessage("start");
```

- Prevents UI freezing during heavy computation

## ➡️ Media API (Audio & Video)

- Play audio/video without plugins.

```js
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>

```

- Used in streaming platforms

## ➡️ Offline & Cache API

- Used for offline web apps.
  - Cache files
  - Works with Service Workers

```js
caches.open("v1").then((cache) => {
  cache.add("/index.html");
});
```

- Used in PWA (Progressive Web Apps)

## ➡️ Canvas API

- Used for 2D graphics, charts, games.

```js
<canvas id="myCanvas"></canvas>
```

```js
const ctx = canvas.getContext("2d");
ctx.fillRect(20, 20, 100, 50);
```

- Used in games, dashboards, image editors

## ➡️ Drag and Drop API

- Allows drag-and-drop behavior

```js
<div draggable="true">Drag me</div>
```

```js
element.addEventListener("dragstart", () => {
  console.log("Dragging");
});
```

- Used in file upload & UI builders
