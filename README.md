# Shake Gesture Detection for Cordova [![npm version](https://badge.fury.io/js/cordova-plugin-neushake.svg)](//npmjs.com/package/cordova-plugin-neushake)

Apache Cordova / PhoneGap Plugin to detect when a physical device performs a shake gesture.

For iOS, the plugin uses the native shake detection.
Fo all other platforms, it is based on a standalone JavaScript implementation I wrote last year ([gist](https://gist.github.com/NeutrinosPlatform/4078996)).

## Install

Requires Cordova v5.0.0 or above.

### Latest published version on npm

```bash
cordova plugin add cordova-plugin-neushake
```

### Latest version from GitHub

```bash
cordova plugin add https://github.com/NeutrinosPlatform/cordova-plugin-neushake.git
```

## Usage

You **do not** need to reference any JavaScript, the Cordova plugin architecture will add a shake object to your root automatically when you build.

**NB:** For non-iOS platforms, there is no native component to this plugin but it depends on the device motion plugin (added when this plugin is added).

## Example

```js
var onShake = function () {
  // Fired when a shake is detected
};

var onError = function () {
  // Fired when there is an accelerometer error (optional)
};

// Start watching for shake gestures and call "onShake"
// with a shake sensitivity of 40 (optional, default 30)
shake.startWatch(onShake, 40 /*, onError */);

// Stop watching for shake gestures
shake.stopWatch();
```

## License

[MIT License](http://ilee.mit-license.org)

## More about us!

Find out more or contact us directly here :- http://www.neutrinos.co/

Facebook :- https://www.facebook.com/Neutrinos.co/ <br/>

LinkedIn :- https://www.linkedin.com/company/25057297/ <br/>

Twitter :- https://twitter.com/Neutrinosco <br/>

Instagram :- https://www.instagram.com/neutrinos.co/
