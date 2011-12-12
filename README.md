clojure-python is a library for Jython interop in Clojure.

Overview
========

Python libraries can be used in Clojure by instantiating 
a Jython interpreter via Clojure's excellent Java interop.
However, the way in which Python code is wrapped by Jython 
makes interop with Python clumsy and verbose. This library 
aims to make Jython interop in Clojure nearly as seamless 
as basic java interop.

Usage and Installation
======================

To experiment with it:
---------------------

0. clone the repository
0. mvn install:install-file -DgroupId=org.python -DartifactId=jython -Dversion=2.5.1 -Dpackaging=jar -Dfile=./etc/jython-2.5.1.jar
   (Because the Maven artifact for Jython 2.5.1 has not yet been added to the central Maven repository, for now it is necessary to install it locally with mvn before running lein deps.) 
0. lein deps
0. lein repl

To include as a dependency:
--------------------------

Copy the config section found at http://clojars.org/clojure-python into your dependencies in your project's project.clj.

Important: it will be necessary to include step #2 above (mvn install...) and the 2.5.1 jar itself in any installation instructions for using this as a dependency, until a recent version of Jython is made available in the central maven repository.

License
=======

Copyright (C) 2010-2012 Robert P. Levy

Distributed under LGPL.