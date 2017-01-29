# What is Gomix? The Programmer Edition

* from [What is Gomix? The Programmer Edition](https://support.gomix.com/t/what-is-gomix-the-programmer-edition/779)

* what can, and can't, do with the platform
    * on the backend it looks like I get server running some sort of server side javascript system (is this NodeJS?). 
    * an in-browser IDE. 
    * a packages.json file which (?) is an NPM file which (?) means can pull in any NPM package into project and then require away. 
    * an NPM packages.json starts up an express server.

* what other things provided?
    * on the backend, the mongodb project (https://gomix.com/#!/project/mongodb4) makes it clear Gomix can talk to these sorts of systems.
      * but does it do anything to help/provide a datastore or other backend systems (MongoDB, PostgreSQL, memcached, MySQL, etc.)? 
      * or is the Gomix mindset more a "run your own datastore elsewhere, and shouldn't you be using someone's API instead?"
    * on the frontend, it's clear Gomix (via Node and express) can serve any file dropped in, so the possibilities are endless.
      * but are there any systems for managing and importing frontend libraries? 
      * or is the Gomix philosophy "use a CDN for that, like we did with jQuery".
    * a lot of modern javascript tools require some sort of "write code in this thing we made up, run some build scripts, and spit out compiled/transpiled/etc. frontend code". 
      * does Gomix have support, or a replacement for, for these sorts of things? 
      * or is the Gomix philosophy "We don't want you trapped at the bottom of Russian Nesting Dolls".


Gomix provides you with your own container that allows you to run both frontend and backend code, edited with a browser-based editor and it takes care of the hosting and deployment for you - providing you with your own URL that's instantly available.

* the backend is just Node.js for now, but we plan to add support for others soon - like Python, Ruby, PHP etc. 
* packages.json does allow you to install any NPM package and they should just work. 
  * you can use Express for your server, that's what many of our examples use, but you could just as easily swap out that package and use hapi.js, Restify, whatever.
* the container you get has a persistent filesystem, so you can store data locally in files as a flat-file database, or store your database files there instead if you're using SQLite (see example: https://gomix.com/#!/project/sqlite3-db7), NeDB (see example: https://gomix.com/#!/project/ne-db6) or something else. But you can choose to use third-party hosted services too (such as https://gomix.com/#!/project/mongodb-sync3). We're thinking about other ways to expose storage options to users as it's a common stumbling point.

* you can use bash scripts and NPM's scripts for frontend build pipelines and command line features. 
* can't currently root access into the container to install stuff on own, but gomix team can add stuff to the base image needed.

see also [Gomix FAQs](https://gomix.com/help/faqs/0
