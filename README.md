Mahabalipuram Shore Temple – Gaussian Splatting Viewer

Live Demo:
https://darkwolf007.github.io/mahabalipuram_GassianSpaltting/

Overview:
This project is a web-based 3D visualization of the Mahabalipuram Shore Temple using Gaussian Splatting (.splat format). It renders high-quality photogrammetry data directly in the browser using WebGL, enabling smooth and interactive viewing without requiring any heavy 3D engines.

Features:
- Real-time rendering of .splat models
- Fully browser-based (no backend required)
- Orbit controls for navigation
- Loading progress indicator
- Lightweight and fast performance

Tech Stack:
- GSplat Renderer (via CDN)
- WebGL
- JavaScript (ES Modules)
- HTML and CSS

Project Structure:
- index.html: Main HTML layout
- index.js: Rendering and loading logic
- style.css: Styling and user interface

How It Works:
1. The .splat model is hosted on a CDN.
2. The application fetches the model using GSplat loader.
3. The model is parsed and rendered using WebGL.
4. Camera and orbit controls allow the user to explore the scene interactively.

Model Loading:
The model is loaded dynamically using the GSplat loader:

const url = "YOUR_SPLAT_FILE_URL";
await SPLAT.Loader.LoadAsync(url, scene, (progress) => {
    progressIndicator.value = progress * 100;
});

Running Locally:
Option 1: Using a simple server
> npx serve

Option 2: Using VS Code Live Server
- Install Live Server extension
- Open index.html with Live Server

Deployment:
This project is deployed using GitHub Pages. Push your code to the main branch and it will be available at:
https://<username>.github.io/<repo-name>/

Notes:
- .splat files can be large (30–50MB), so using a CDN is recommended.
- Ensure CORS is enabled if hosting externally.
- If the model fails to load, try clearing browser cache or doing a hard refresh.

Future Improvements:
- Progressive streaming for large models
- Mobile optimization
- Support for multiple scenes
- UI enhancements and controls

Credits:
- GSplat library for Gaussian Splatting rendering
- Photogrammetry data for Mahabalipuram Shore Temple

License:
MIT License (or specify your own)
