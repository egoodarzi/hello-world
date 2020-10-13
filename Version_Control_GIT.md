# GIT

- keeps meta data (authors, timestamps)
## why useful
 - keep track of files even in personal projects
 like homework assignments
 - collaborating, working with others
 - who wrote a particular madule or editted it or ...
 - go back in time
 - automaticaly find errors !
 - GIT is de-facto standard for version control
 
 [image of crazy job with GIT :)](https://xkcd.com/1597/)
 
 the best way to learn git is not by starting from its interface, it has a terribbly designed interface!
 
 its underlying design and ideas are pretty beautiful! it is better to understand them. we first start with its data model. then to commands.
 
 ## git graph history
 we have files and folders.
 
 - folders are called **tree**s.
 
 trees can contain other trees or trees and files.
 - files are called **blob**s. 
  obviously files can't contain trees
 
 
the top-level tree is the directory being tracked

### how do we snapshot this tree?
git uses a directed asyclic graph to model history!

 in git each snapshot has some number of parents, and basically want to know what change preceded what other change.
 
 snapshot contains the entire content of the tree. (root tree)
 [explain the diagram of history]
 fork to branches and sync with master branch.
 each circle stands for kind of a snapshot (tree with files and folders) but they also have metadata.(author, message, ..)
 
 
 ### we want to go one level lower than this!
 how exactly is this represented as a data structure inside GIT.
 ```
 type blob = array<bytes>
 type tree = map<string, tree | blob>   # mapping between filename and its content(string and tree)
 type commit = struct  # a bunch of staff
      parents: array<commits>    # commits have normally one parent, elif merge commits which have multiple parents
      author: string
      message: string
      snapshot: tree
 ```

type object = blob | tree | commit
objects = map<string, object>

store the object on disk, what you store is a hash of the object,

store object in sudocode:
```
def store(o):
   id = sha1(o)   # compute its id by sha 1 hash
   object[id] = o  # put it into object map, stored to disk
```
roughly what hash is doing is this: give it a large file, it gives you a short name for it. it creates a string. hexadecmal strings of 40 characters long.(160 bit hash)

load objects from store:
```
def load(id):
    return object[id]
```

they are actually pointers to objects.

now we have a way of identifying unified all the different types of objects to one type of thing we call object.

and we have a wa y of identifying objectrs by their sha1 hash.

### solution to naming
 ids are 40 hexadecimal characters. long and ugly!
 
 it maintains objects and refrences. what are refrences?
 
 #### refrences
 ```
 refrence = map<string, string>   # map from string to string.
 ```
 maps human readable string to id's.
 
 for example:  "fix previous bug" --> id(40 character long hexadecimal string)
 
 now we can refer to particular snapshot in the history.
 
 ### about graph
 given GIT design of history, it look like immutable. 
 
 you can add new staff to it but you can not manupulate anything thing in it.

# GIT commands
objects and refrences, that all there is to a GIT repository. the two pieces of data that it stores.

all GIT commandline commands are just manipulations of either the refreneces data or the objects data.

```git
mkdir demo
cd demo
git init   # initializez GIT
ls         # nothing is there yet
ls -a      # there is a hidden file. 
ls .git    # it contains a bunch of stuff in it. GIT stores its internal data, objects and refrensces.
git help init
sit status

```
