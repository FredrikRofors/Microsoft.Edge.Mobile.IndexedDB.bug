# Microsoft.Edge.Mobile.IndexedDB.bug

This project is used to demo a bug found in the Microsoft Edge Mobile browser for iOS. 

The project consists of a sigle index.html page with a simple file upload. 
After selecting a file, the file is stored in IndexedDB (PhotoApp -> OfflineFiles) using "native" or plain vanilla JavaScript (no 3rd party libraries) and the <a href="https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API" target="_blank">IndexedDB browser API</a>.

If you want to try it out on your local machine, follow these steps:
<ol>
    <li>Clone this repo.</li>
    <li>Run 'npm install' to install <a href="https://www.npmjs.com/package/http-server" target="_blank">http-server</a>, a simple Node based static HTTP server. </li>
    <li>Run 'npx http-server' to spin up the localhost HTTP server.</li>
    <li>Open a browser and navigate to <a href="http://localhost:8080" target="_blank">http://localhost:8080</a> to play with the demo app.</li>
</ol>

## Bug description
[Content goes here]

## Browsers where the bug manifests itself
<ul>
    <li>Microsoft Edge Mobile for iOS (connected to a work account</li>
</ul>

## Browsers where the bug is NOT present
<ul>
    <li>Microsoft Edge Mobile for iOS (not connected to a work account)
    <li>Microsoft Edge Desktop for Windows</li>
    <li>Chrome for Windows</li>
    <li>Chrome for iOS
</ul>

