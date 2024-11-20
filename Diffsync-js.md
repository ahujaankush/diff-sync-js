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

- Where / How is the edit-Stack implemented?
  
  

- Is it possible to deploy a Peer-to-Peer Version of Mr.Wei´s implementation?

- How is it possible to use the API in other JS-Projects?
  
  We get the API from the diff-sync. We can use the functions to implement it in our code that can help us to merge data.

- Are the Json-Docs interchangable with other kind of Docs?

- How is Mr.Wei solving the complicts?

- What are possible enhancements of Mr.Wei´s Code? Should you suggest a pull-request?


