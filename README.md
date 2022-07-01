# fast guide

- Clone
- `cd PhysSample`
- `npm install`
- copy folder `app_package\recast` into `app_package\node_modules`
- `npm run dev`

This will launch a watcher and a web browser. You should see the plane and the sphere.
Open the browser console and you should see :

```
[HMR] Waiting for update signal from WDS...
playgroundRunner.js:8 Assets host URL: http://127.0.0.1:8181/
thinEngine.js:415 Babylon.js v5.13.3 - WebGL2 - Parallel shader compilation
index.js:551 [webpack-dev-server] Hot Module Replacement enabled.
index.js:551 [webpack-dev-server] Live Reloading enabled.
playground.js:55 Vec3 {ptr: 5272312}
```

Important line is `Vec3 {ptr: 5272312}`. This is a Vec3 instance from a class defined in the plugin.
The corresponding code is in `app_package\src\Playground\playground.ts`

Any time you change and save a file, like playground.ts, this will trigger a typescript compilation and a browser refresh thanks to the watcher.
