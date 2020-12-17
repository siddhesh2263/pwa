# Progressive Web Apps - Introduction

This application uses Materialise CSS.
One important component is the manifest.json file, which describes the presetation details of the app.

This is a tutorial application, I hope to build mine soon.

## Service Workers
They allow us to do:
1. Load content offline
2. Use background sync
3. Use push notifications

* They are Javascript files. They are separate threads.

* They work in background, disconnected from the DOM, such as listen for fetch reuests, push messgaes etc. They sit in the background, and react to different process. They are different from main thread.

## Service Worker Lifecycle

* app.js registers the service worker (sw.js), which then the browser installs the event. Then the service workeer becomes activem and then the service worker listens for events.

* On page reload, since the sw is already registered and installed, it will directly listen for events. No need to install event again.

* In case the sw.js file is changed, the sw is registered again, and is installed. But it waits till the previous sw completes all its tasks. Once completed, the new sw is activated.
