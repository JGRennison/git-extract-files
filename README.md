## git-extract-files
**Create a new history of the current branch containing only the specified files/directories**  

### Usage:

    git extract-files [options] files...

This creates a new history of the current branch, containing only the specified files/directories.  
The commit hash of the new history is written to STDOUT, and optionally a branch is created which points to it.  
Optionally, files/directories may be excluded or moved to a different path within the new history.  
This does not touch the index or working tree, and is significanty more performant than git filter-branch.

### Options:
* -l, --list-file *path*  
  Extract files enumerated in list file, one file name per line.  
  This may be used more than once.
* -s, --source *ref*  
  Use 'ref' instead of HEAD as the source commit.
* -m, --move *from:to*  
  Move files from absolute path 'from' to 'to'.  
  This may be used more than once. However only the first matching move for an individual file is applied.
* -x, --exclude *path*  
  Exclude files from absolute path.  
  This may be used more than once.  
  Excludes are applied before moves.
* -b, --branch *branch*  
  Create a new branch pointing to the new commit
* -u, --until *rev*  
  Do not re-write commits reachable from 'rev'.  
  This may be used more than once.
* -r, --remove *rev*  
  Remove commits reachable from 'rev'.  
  This may be used more than once.
* -f, --fixup *rev*  
  Apply commit 'rev' as a fixup (if it has one parent).  
  This may be used more than once.
* -n, --no-prune  
  Don't prune empty commits which leave the tree untouched, this keeps all commits in the input.
* -c, --keep-committer  
  Preserve committer name, email and date
* -p, --add-parent *rev:parent*  
  Add a new parent to commit 'rev'
* -v, --verbose  
  Be verbose
* -h, -?, --help  
  Show help

### Dependencies:
* Perl 5:  
  * Proc::Hevy  
  * Getopt::Long

### URLs:
This project is hosted at https://github.com/JGRennison/git-extract-files

### License:
New BSD License, see LICENSE.txt
