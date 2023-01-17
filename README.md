# Microsoft.Edge.Mobile.IndexedDB.bug

This project is used to demo a bug found in the Microsoft Edge Mobile browser for iOS. 

The project consists of a sigle index.html page with a simple file upload. 
After selecting a file, the file is stored in IndexedDB (PhotoApp -> OfflineFiles) using "native" or plain vanilla JavaScript (no 3rd party libraries) and the <a href="https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API" target="_blank">IndexedDB browser API</a>.

You can <a href="https://fry-edge-mobile-indexeddb-bug.s3.eu-west-1.amazonaws.com/index.html" target="_blank">try out the demo app here</a>
or setup it up on your local machine follow these steps:
<ol>
    <li>Clone this repo.</li>
    <li>Run 'npm install' to install <a href="https://www.npmjs.com/package/http-server" target="_blank">http-server</a>, a simple Node based static HTTP server. </li>
    <li>Run 'npx http-server' to spin up the localhost HTTP server.</li>
    <li>Open a browser and navigate to <a href="http://localhost:8080" target="_blank">http://localhost:8080</a> to play with the demo app.</li>
</ol>

## Bug description
When Microsoft Edge Mobile browser on iOS is connected to a work account, the Javascript code storing the file to IndexedDB silently fails (no errors). Subsequent calls to IndexedDB to retrieve the keys stored in the IndexedDB returns 0 (no keys). If the Edge browser is disconnected to the work account all works well.

## Browsers where the bug manifests itself
<ul>
    <li>Microsoft Edge Mobile (ver 108.0.1462.77) for iOS (connected to a work account)</li>
</ul>

## Browsers where the bug is NOT present
<ul>
    <li>Microsoft Edge Mobile for iOS (NOT connected to a work account)
    <li>Microsoft Edge Desktop for Windows</li>
    <li>Chrome for Windows</li>
    <li>Chrome for iOS
</ul>

