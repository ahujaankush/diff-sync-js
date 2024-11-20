# Diffsync-js

- Which implementation of diff-patch-Alg?
  
  Mr. Wei's `diff-sync-js` implementation utilizes the `fast-json-patch`.  The Diff Match Patch library provides robust algorithms for computing differences between texts and applying patches.
  
  "Section 3 and Section 7"

- Where are the documents of the shadows
  
  Server Side: Shadows are stored in the `DiffSyncAlgorithm`
  
  Client Side: Shadows are maintained locally within the client synchronization logic, where diffs are computed against the shadow before sending them to the server.
  
  ```js
  var diffSync = new DiffSyncAlghorithm({
      jsonpatch: jsonpatch,
      thisVersion: "m",
      senderVersion: "n",
      useChecksum: true
  });
  ```

- How and why can we adjust the sync-cycle? What are the disadvantages?
  
  Here we can adjust it:
  
  } else {  
      interval = setInterval(() => {  
          $textfield.value = $textfield.value + i++ + ",";  
          sendPatch($textfield.value);  
      }, 300);  
  }
  
  Why adjust?:
  
  Faster Cycle: Improves real-time responsiveness.
  
  Slower Cycle: Reduces server load and network traffic.
  
  Disadvantages:
  
  Too Fast: Increases network and CPU usage, risking server overload.
  
  Too Slow: Leads to delayed updates, causing a poor user experience.

- Where / How is the edit-Stack implemented?
  
  

- Is it possible to deploy a Peer-to-Peer Version of Mr.Wei´s implementation?

- 

- How is it possible to use the API in other JS-Projects?
  
  We get the API from the diff-sync. We can use the functions to implement it in our code that can help us to merge data.

- Are the Json-Docs interchangable with other kind of Docs?

- The implementation is optimized for JSON documents and relies on `fast-json-patch` for computing and applying diffs.

- How is Mr.Wei solving the complicts?
  
  The implementation uses version numbers `thisVersion` and `senderVersion` to track changes and ensure edits are applied in the correct order.

- What are possible enhancements of Mr.Wei´s Code? Should you suggest a pull-request?


