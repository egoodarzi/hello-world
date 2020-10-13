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
 '''
 type blob = array<bytes>
 type tree = map<string, tree | blob>   # mapping between filename and its content(string and tree)
 type commit = struct  # a bunch of staff
      parents: 
 '''
 
 
