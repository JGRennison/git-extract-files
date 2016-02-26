## git-extract-files
**Create a new history of the current branch containing only the specified files/directories**  

### Usage:

    git extract-files [options] files...

This creates a new history of the current branch, containing only the specified files/directories.  
The commit hash of the new history is written to STDOUT, and optionally a branch is created which points to it.  
Optionally, files/directories may be moved to a different path within the new history.

### Options:
* -m, --move *from:to*  
  Move files from absolute path 'from' to 'to'.  
  This may be used more than once.
* -b, --branch *branch*  
  Create a new branch pointing to the new commit
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
