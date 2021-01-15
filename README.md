This repo demonstrates an inconsistency between running Gatsby in develop mode versus the production build. Steps to reproduce:

1. After checking the repo out, run `npm install && gatsby develop`
2. Go to [http://localhost:8000/](http://localhost:8000/)
3. Observe the **red** background of the div containing the string. This is unexpected because `src/pages/index.js` does not import `src/styles/red.css`, only `src/pages/red.js` does.
4. Stop the develop server and run `gatsby build && gatsby serve`
5. Go to [http://localhost:9000/](http://localhost:9000/)
6. Observe the **white** background of the div containing the string. This is in stark contrast with step 3, therefore the inconsistency.