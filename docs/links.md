
#### cljs self- hosting/compiling

- http://swannodette.github.io/2015/07/29/clojurescript-17/
- https://clojurescript.org/guides/self-hosting
- https://github.com/anmonteiro/lumo
    - https://anmonteiro.com/2017/02/compiling-clojurescript-projects-without-the-jvm/
- https://github.com/planck-repl/planck

#### cljs

- cljs 1.10.749 Embracing JavaScript Tools
    - https://clojurescript.org/news/2020-04-24-bundle-target
    - https://clojurescript.org/guides/webpack
    - implications for sahdow-cljs
        - https://code.thheller.com/blog/shadow-cljs/2018/06/15/why-not-webpack.html
        - https://github.com/thheller/shadow-cljs/issues/706
            - 'Why not Webpack?' is still the answer, despite :bundle target
            - nevertheless, updated answer
                - https://code.thheller.com/blog/shadow-cljs/2020/05/08/how-about-webpack-now.html

#### lein-cljsbuild

- https://github.com/emezeske/lein-cljsbuild
- https://github.com/emezeske/lein-cljsbuild/blob/1.1.8/sample.project.clj
- https://github.com/emezeske/lein-cljsbuild/blob/1.1.8/example-projects/advanced/project.clj


#### figwheel-main

- https://figwheel.org/docs/editor-integration.html
- https://github.com/bhauman/figwheel-main


#### vscode debug multiple extensions

- the argument --extensionDevelopmentPath can now be specified more than once.
    - https://github.com/microsoft/vscode/issues/72500
- https://code.visualstudio.com/docs/editor/debugging#_compound-launch-configurations
- https://code.visualstudio.com/docs/nodejs/nodejs-debugging#_launch-configuration-attributes


#### vscode error : Proposed api on trying to log some vscode ref

- happens when (println {:context vscode-context-ref)

```
Error: [https://github.com/DeathStarGame/deathstar.ltee.deathstar.ltee]: Proposed API is only available when running out of dev or with the following command line switch: --enable-proposed-api https://github.com/DeathStarGame/deathstar.ltee.deathstar.ltee    at a (/usr/share/code/resources/app/out/vs/workbench/services/extensions/node/extensionHostProcess.js:605:324)    at Object.checkProposedApiEnabled (/usr/share/code/resources/app/out/vs/workbench/services/extensions/node/extensionHostProcess.js:605:686)    at Object.get logUri [as logUri] (/usr/share/code/resources/app/out/vs/workbench/services/extensions/node/extensionHostProcess.js:876:651)
```

- or same but for js/console.log 

```
[Extension Host] Unable to log remote console arguments Output omitted for an object that cannot be inspected ('Error: [https://github.com/DeathStarGame/deathstar.ltee.deathstar.ltee]: Proposed API is only available when running out of dev or with the following command line switch: --enable-proposed-api https://github.com/DeathStarGame/deathstar.ltee.deathstar.ltee')
```

- simple, but deadly - as it's unclear what causes it
- takeaway: don't log left and right vscode stuff


#### nodejs worker_threads

- https://nodejs.org/api/worker_threads.html
- https://blog.soshace.com/advanced-node-js-a-hands-on-guide-to-event-loop-child-process-and-worker-threads-in-node-js/
- https://nodesource.com/blog/worker-threads-nodejs/
- https://blog.logrocket.com/node-js-multithreading-what-are-worker-threads-and-why-do-they-matter-48ab102f8b10/


#### java sockets

- https://stackoverflow.com/questions/8406914/benefits-of-netty-over-basic-serversocket-server
- https://stackoverflow.com/questions/5385407/whats-the-difference-between-jetty-and-netty
- libs
    - https://github.com/TooTallNate/Java-WebSocket
    - https://github.com/socketio
        - https://github.com/socketio/engine.io-server-java 
        - https://github.com/socketio/socket.io-client-java


#### nrepl middleware

- how default middleware is added
    - https://github.com/nrepl/nrepl/blob/master/src/clojure/nrepl/server.clj#L85
- how cider adds its middleware to nrepl's default
    - https://github.com/clojure-emacs/cider-nrepl/blob/master/src/cider/nrepl.clj#L527