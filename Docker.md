# Information I gathered on how to make a dockerfile that installs a working metatrader instance



## Needed:
- wine (makes it possible to run certain windows applications on linux machines)
- Copy of metatrader setup or a copy of the install directory because running metatrader setup in dockerfile doesn't seem to be working even in silent mode (meaning through terminal with default setup)
- virtual display because metatrader can or cannot run headless (not sure yet)




## Docker file settings needed
```DEBIAN_FRONTEND=noninteractive``` = some installations ask for options while installing like a location i.e. to use this tag before the installation command it skips these steps so the docker file can install it without waiting for the questions.



running metatrader with x11 server for gui because metatrader needs it
```ENV DISPLAY=host.docker.internal:0.0``` when addind this to the dockerfile it creates a window on the host machine (windows 10) when docker is run. You need to install a x server on the host machine (windows 10) like xming or xlaunch (only xlaunch worked for me).
