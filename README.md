![alt text](https://cordova.apache.org/static/img/artwork/cordova_logo_normal_dark_large.png)
# cordova-media-plugin

This plugin provides the ability to play audio files on a device.
This plugin defines a global Media Constructor.
Although in the global scope, it is not available until after the deviceready event.
```Javascript
document.addEventListener("deviceready", onDeviceReady, false);
function onDeviceReady() {
    console.log(Media);
}
```
## Object Media

```Javascript
var media = new Media(src, mediaSuccess, [mediaError], [mediaStatus]);
```
* **src**: A URI containing the audio content. (DOMString)
* **mediaSuccess**: (Optional) The callback that executes after a Media object has completed the current play, record, or stop action. (Function)
* **mediaError**: (Optional) The callback that executes if an error occurs. (Function)
* **mediaStatus**: (Optional) The callback that executes to indicate status changes. (Function)

## Constants

The following constants are reported as the only parameter to the mediaStatus callback:

* `Media.MEDIA_NONE` = 0;
* `Media.MEDIA_STARTING` = 1;
* ``Media.MEDIA_RUNNING`` = 2;
* ``Media.MEDIA_PAUSED`` = 3;
* ``Media.MEDIA_STOPPED`` = 4;

## Methods

* ``media.getCurrentAmplitude``: Returns the current position within an audio file.
* ``media.getCurrentPosition``: Returns the current position within an audio file.
* ``media.getDuration``: Returns the duration of an audio file.
* ``media.play``: Start or resume playing an audio file.
* ``media.pause``: Pause playback of an audio file.
* ``media.pauseRecord``: Pause recording of an audio file.
* ``media.release``: Releases the underlying operating system's audio resources.
* ``media.resumeRecord``: Resume recording of an audio file.
* ``media.seekTo``: Moves the position within the audio file.
* ``media.setVolume``: Set the volume for audio playback.
* ``media.startRecord``: Start recording an audio file.
* ``media.stopRecord``: Stop recording an audio file.
* ``media.stop``: Stop playing an audio file.

For further information visit the [Cordova Documentation](https://cordova.apache.org/docs/en/latest/reference/cordova-plugin-media/)
