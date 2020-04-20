### This is my port of example from the tutorial: https://github.com/8Observer8/phaser3-webpack-es6-dev-starter

Run on Playground: https://plnkr.co/edit/Z6sBTY82TQXwIlah?preview

This is a port to TypeScript. You can set breakpoints (use Chrome addon for VSCode). You can publish your example on Plunker. I use RequireJS for debugging and publishing on Playground. And I use Browserify and UglifyJS for creating a bundle for release.

### Install:
> npm i

Note. You need to open the file `node_modules\phaser\types\phaser.d.ts`. Go to the end of the file and rename this:

```
declare module 'phaser' {
    export = Phaser;

}
```

to this:
```
declare module 'Phaser' {
    export = Phaser;

}
```

### Debug version:
> npm run debug

### Release version:
> npm run release

### Note. See comments in `index.html` to switch between `Debug` and `Release` versions. For example, if you want to switch to `Release` version you just need to comment `Debug version` and uncomment `Release version` and recompile the project: `npm run release`

```js
    <!-- Debug version -->
    <script data-main="js/RequireConfig" src="https://dl.dropboxusercontent.com/s/kgepxh66w1j8d8f/require-2.3.6.min.js"></script>

    <!-- Release version -->
    <!-- <script src="js/bundle.min.js"></script> -->

```
