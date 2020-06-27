# brickbreaker-merged
Version of brick breaker game which will run from a local file without causing web security issues (CORS, Strict MIME etc)

There is an outstanding javascript game tutorial at https://www.youtube.com/watch?v=3EMxBkqC4z0&t=51s which creates a great object oriented game architecture for javascript based games. I highly recommend it.

It was developed on codesandbox ( https://codesandbox.io/s/z2pqr9620m ) and if you download the zip file from codesandbox and try and run the code (ie double click on index.html) without a server it fails with CORS errors in the latest browsers (as at 2020).

In order to be able to run the game code without requiring a server, I have restructured the Brick Breaker Game code as SINGLE javascript file and removed the imports and export clauses which circumvents any cross file security issues. All the object oriented structure is maintained correctly.
 
To run the game simply download the zip from this github repository (green button at top right) and unzip into any folder, Then double click on the index.html file and the game will run on Chrome, Firefox, Safari.

Note for developers - you can run this within Sublime text and VS Code without any problems.

Notes
 - in the merged javascript file, brickgame-merged.js, the sequence of classes is very important
 - the web security issues have to do with the requirement for 'same origin' for all the files
   imports and exports involve several files eg ball.js, paddle.js etc which are not considered
   as having the same origin. By merging all the javascript into one file the browser sees all the
   code as having the same origin
 - Any bugs in the original code still exist in this code
