# Lite-Git

To initialize the repository-

~lite init <filename>






To use Checkout, List Tree, Inspecting an object-
make a new text file in a folder
use add (git add test_file.txt)
commit the file (git commit -m "initial commit")
run there commands in the just file commited directory

Checkout:
make a new directory(let us say new_empty_directory)
run-
~lite checkout master ~/new_empty_directory

List Tree:
~lite ls-tree -r HEAD

Inspect an Object:
~lite cat-file blob <hash>
[The hash will be the has code we get after running List Tree command]





The rev-parse command-
Navigate to a valid git repository where some files are commited with a .git folder and run the following commands in directory:

~lite rev-parse --wyag-type commit HEAD <!-- Resolves the hash of the commit object that HEAD points to>
~lite rev-parse --wyag-type tree HEAD <!-- Resolves the hash of the tree object associated with HEAD>
~lite rev-parse --wyag-type tag HEAD <!-- Tries to resolve a tag object associated with HEAD, if None is output it indicates HEAD is not pointing to a tag>






Checking ignore and Status-
Navigate to a valid git repository where .gitignore is being tracked(git add .gitignore) and run the following commands in the directory:

Checking Ignore:
~lite check-ignore <file-name> <!-- if the file-name's extension is mentioned in the .gitignore then the file-name will be printed else not>

Checking Status:
~lite status

Add Files-
~lite add <file-name>

Commit Files-
~lite commit -m "message"
