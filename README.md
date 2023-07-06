To create a donut shape in Three.js, you can use the `THREE.TorusGeometry` class. Here's an example code snippet to create a donut:

```javascript
// Create a scene
var scene = new THREE.Scene();

// Create a camera
var camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
camera.position.z = 5;

// Create a renderer
var renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

// Create a torus geometry
var geometry = new THREE.TorusGeometry(1, 0.5, 16, 100);

// Create a material
var material = new THREE.MeshBasicMaterial({ color: 0xff00ff });

// Create a mesh and add it to the scene
var torus = new THREE.Mesh(geometry, material);
scene.add(torus);

// Render the scene
function animate() {
   requestAnimationFrame(animate);
   torus.rotation.x += 0.01;
   torus.rotation.y += 0.01;
   renderer.render(scene, camera);
}
animate();
```

In this code, we create a `TorusGeometry` with the parameters specifying the radius, tube radius, radial segments, and tubular segments of the donut shape. Then, we create a `Mesh` with the torus geometry and a material, and add it to the scene. Finally, we use the `requestAnimationFrame` function to animate the donut by updating its rotation and rendering the scene.
