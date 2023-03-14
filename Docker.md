# Information I gathered on how to make a dockerfile that installs a working metatrader instance



## Needed:
- wine (makes it possible to run certain windows applications on linux machines)
- Copy of metatrader setup or a copy of the install directory because running metatrader setup in dockerfile doesn't seem to be working even in silent mode (meaning through terminal with default setup)
- virtual display because metatrader can or cannot run headless (not sure yet)
