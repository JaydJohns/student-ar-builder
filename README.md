# AR Builder - Student Collaborative 3D Creation Tool

A web-based A-Frame AR builder that lets groups of students collaboratively create and view 3D scenes in augmented reality—no login required, works on any phone browser.

## Features

✅ **Zero Setup** - Just open a URL, no app installation
✅ **Mobile & Desktop** - Works on phones and computers with touch + mouse support
✅ **Multi-Group Support** - Each group gets their own workspace via unique URL
✅ **Drag-and-Drop** - Click and drag to position objects in 3D space
✅ **AR Viewing** - View your scene in real-world AR with WebXR
✅ **Scene Sharing** - Export scenes as shareable links
✅ **Free Hosting** - Deploy to GitHub Pages in minutes

## Quick Start

### 1. Deploy to GitHub Pages (5 minutes)

1. Create a new GitHub repository (e.g., `student-ar-builder`)
2. Upload all files from this folder to the repository
3. Go to **Settings → Pages**
4. Select **Deploy from branch** and choose `main` branch
5. Your site will be live at: `https://yourusername.github.io/student-ar-builder/`

### 2. Generate QR Codes for Your Groups

For each group, create a QR code pointing to:

- **Group 1:** `https://yourusername.github.io/student-ar-builder/?group=1`
- **Group 2:** `https://yourusername.github.io/student-ar-builder/?group=2`
- **Group 3:** `https://yourusername.github.io/student-ar-builder/?group=3`
- **Group 4:** `https://yourusername.github.io/student-ar-builder/?group=4`

Generate QR codes free at: https://www.qr-code-generator.com/

### 3. Workshop Day

1. Print QR codes, one per group
2. Students scan → Opens their group's workspace
3. Click buttons to add objects (Box, Sphere, Cylinder, etc.)
4. Drag objects to move them around
5. Click "View in AR" button to see in real-world AR
6. Click "Export Scene" to get a shareable link
7. Click "Download Scene Data" to save as JSON

## How to Use

### Adding Objects
- Click any colored button at the bottom to add a new 3D object
- Objects appear in the scene

### Moving Objects
- **Desktop:** Click and drag objects to move them
- **Mobile:** Tap and drag objects

### Viewing in AR
- Click the "🥽 View in AR" button
- Point your phone at the floor/table
- See your 3D creation overlaid on the real world
- Touch and drag still works in AR mode

### Exporting
- **Share Link:** Click "📤 Export Scene" to copy a shareable link to clipboard
- **Download:** Click "⬇️ Download Scene Data" to save as JSON file

### Clearing
- Click "🗑️ Clear All" to remove all objects (with confirmation)

## Available Objects

- **Box** (📦) - Red
- **Sphere** (⚪) - Blue
- **Cylinder** (🔶) - Orange
- **Cone** (🔺) - Purple
- **Plane** (📄) - Cyan
- **Dodecahedron** (🔷) - Dark Orange

## Browser Support

✅ **Mobile:** Chrome, Firefox, Safari (iOS 14.5+)
✅ **Desktop:** Chrome, Firefox, Edge, Safari

**AR support:** Requires WebXR-capable browser:
- Android: Chrome, Firefox
- iOS: Safari 14.5+

## File Structure

```
ar-builder/
├── index.html      # Main application
└── README.md       # This file
```

## What's Inside index.html

- **A-Frame 1.4.2** - 3D scene rendering
- **Three.js** - 3D raycasting & interaction
- **JavaScript** - Drag/drop, AR mode, scene export
- **Responsive CSS** - Mobile-friendly UI

## Customization

### Change Available Objects
Edit this section in `index.html`:

```html
<button class="asset-btn" onclick="addObject('box', '#e74c3c')">📦 Box</button>
```

- First parameter: A-Frame primitive (box, sphere, cylinder, cone, plane, dodecahedron)
- Second parameter: Color hex code

### Change Colors
Modify the color hex code in each button.

### Add Your Own 3D Models
To add custom models, modify the `addObject()` function to use:

```javascript
entity.setAttribute('gltf-model', 'url-to-your-model.glb');
```

Find free models at: https://sketchfab.com/ (download as GLB)

## Troubleshooting

**"AR not working"**
- Requires WebXR support - test at: https://immersiveweb.org/
- Chrome on Android works best

**"Objects not dragging"**
- Make sure you're clicking directly on the object
- Try on desktop first, then mobile

**"Scene won't load from link"**
- The link must be complete. Make sure `?scene=...` is included

## Technical Notes

- Scene data is encoded in the URL using Base64
- Maximum URL length is ~2000 characters (limits scene complexity)
- No backend/database - everything client-side
- Works offline once loaded

## Workshop Tips

1. **Warm-up:** Have groups add a few objects before going live
2. **Time-box AR viewing:** Give 5 minutes for AR exploration
3. **Documentation:** Have students screenshot their creation
4. **Share:** Display each group's scene link on a big screen
5. **Challenge:** "Who can build the tallest structure?" etc.

---

Built with A-Frame & Three.js | Designed for student collaboration | Zero cost to host