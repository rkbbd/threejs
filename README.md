
This Project has some example of Threejs

Example 1: [Dhaka tour](https://threejs.org/examples/)<br />
Example 2: [Box Geometry](https://github.com/rkbbd/threejs/tree/master/Box%20Geometry)<br />
Example 3: [Earth](https://github.com/rkbbd/threejs/tree/master/Earth)<br />
Example 4: [Extrude Geometry](https://github.com/rkbbd/threejs/tree/master/Extrude%20Geometry)<br />
Example 5: [Geometry Example](https://github.com/rkbbd/threejs/tree/master/Geometry%20Example)<br />
Example 6: [Line](https://github.com/rkbbd/threejs/tree/master/Line)<br />
Example 7: [Text](https://github.com/rkbbd/threejs/tree/master/Text)<br />
Example 8: [ball](https://github.com/rkbbd/threejs/tree/master/ball)<br />
Example 9: [bird](https://github.com/rkbbd/threejs/tree/master/bird)<br />
Example 10: [cloth](https://github.com/rkbbd/threejs/tree/master/cloth)<br />
Example 11: [star](https://github.com/rkbbd/threejs/tree/master/star)<br />

```javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>My first three.js app</title>
		<style>
			body { margin: 0; }
		</style>
	</head>
	<body>
		<script src="js/three.js"></script>
		<script>
			const scene = new THREE.Scene();
			const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

			const renderer = new THREE.WebGLRenderer();
			renderer.setSize( window.innerWidth, window.innerHeight );
			document.body.appendChild( renderer.domElement );

			const geometry = new THREE.BoxGeometry();
			const material = new THREE.MeshBasicMaterial( { color: 0x00ff00 } );
			const cube = new THREE.Mesh( geometry, material );
			scene.add( cube );

			camera.position.z = 5;

			const animate = function () {
				requestAnimationFrame( animate );

				cube.rotation.x += 0.01;
				cube.rotation.y += 0.01;

				renderer.render( scene, camera );
			};

			animate();
		</script>
	</body>
</html>
```
