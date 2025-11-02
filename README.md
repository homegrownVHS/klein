# Hyperbolic Space Journey - Three.js Art Installation

An immersive 3D art experience that takes you on a journey inside a massive hyperbolic space filled with thousands of colorful, textured cubes.

## Overview

This project creates an artistic interpretation of hyperbolic geometry, placing the viewer inside an infinite-feeling space composed of countless animated cubes. The camera automatically moves along a winding path through this space, creating a meditative and visually stunning experience.

## Features

- **Immersive Hyperbolic Space**: Thousands of cubes arranged in exponentially growing layers
- **Automatic Camera Journey**: Smooth movement along a predefined path through the space
- **Realistic Materials**: Colorful, textured cubes with varying opacity and shininess
- **Dynamic Lighting**: Multiple colored point lights creating atmospheric illumination
- **Organic Animation**: Cubes rotate and oscillate with subtle variations
- **Hyperbolic Distribution**: Mathematical arrangement creating infinite-feeling space
- **Artistic Interpretation**: Focus on visual beauty rather than strict mathematical accuracy

## Quick Start

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Start Development Server**:
   ```bash
   npm run dev
   ```

3. **Open in Browser**:
   Navigate to `http://localhost:3000`

## Artistic Concept

This installation explores the concept of hyperbolic space through artistic interpretation:

- **Exponential Growth**: Each layer contains exponentially more cubes than the previous
- **Hyperbolic Distribution**: Cubes are positioned using polar coordinates with exponential radius scaling
- **Immersive Experience**: The viewer is placed inside the space rather than observing from outside
- **Infinite Feeling**: The exponential distribution creates the sensation of infinite depth

## Project Structure

```
klein/
├── index.html          # Main HTML file
├── css/
│   └── style.css      # Styling and responsive design
├── js/
│   └── main.js        # Three.js implementation and Klein bottle math
├── package.json       # Dependencies and scripts
└── README.md          # This file
```

## Experience

- **Automatic Journey**: No user controls - simply watch and experience
- **Camera Path**: Winding movement through the hyperbolic space
- **Looping Animation**: The journey repeats seamlessly
- **Immersive View**: Wide field of view (90°) for maximum immersion
- **Atmospheric Effects**: Fog and lighting enhance the sense of depth

## Technologies Used

- **Three.js**: 3D graphics and WebGL rendering
- **Parametric Geometry**: Mathematical surface generation
- **Orbit Controls**: Interactive camera movement
- **HTTP Server**: Local development server

## Technical Implementation

The hyperbolic space is generated using exponential distribution algorithms:

```javascript
// Hyperbolic distribution with exponential growth
for (let layer = 0; layer < 15; layer++) {
    const radius = Math.pow(1.8, layer); // Exponential growth
    const cubesInLayer = Math.floor(20 * Math.pow(1.5, layer));
    
    // Polar coordinate distribution
    const theta = (i / cubesInLayer) * Math.PI * 2;
    const phi = Math.random() * Math.PI * 2;
    const r = radius + (Math.random() - 0.5) * radius * 0.3;
}
```

## Customization

To modify the hyperbolic space:
1. Edit the `createHyperbolicSpace()` function in `js/main.js`
2. Adjust the `layer` count for more/fewer cubes
3. Modify the exponential growth rate (currently 1.8)
4. Change colors in the `createMaterials()` function
5. Adjust the camera path in `setupCameraPath()`

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

Requires WebGL support for 3D rendering.

## License

MIT License - Feel free to use this code for educational or personal projects.

---

**Note**: This project is an artistic interpretation of hyperbolic geometry, prioritizing visual beauty and immersive experience over mathematical precision. It's designed as a meditative journey through infinite geometric space.