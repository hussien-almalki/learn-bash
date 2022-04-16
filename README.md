# The Find Command
---

**find - search for files in a directory hierarchy**

what we will learn in the section?

* How to use the *`find`* command's default behaviour.
* How control searh *`depth`*.
* How to search by *`type`* (files or directories).
* How to search by *`name`*.
* How to search by *`file size`*.

* `find . ` dot . mean this direcotory.
* `find /`
* `find . -maxdepth 1`  max 100
* `find . -type f`
* `find . -maxdepth 1 -type f`
* `find /etc -maxdepth 1 -type f`
* `find . -name "*.txt*"`
* `find . -maxdepth 1 -name "*.txt*"`
* `find . -maxdepth 1 -iname "*.txt*"`
* `find / -type f -size +100k`
* `find / -type f -size +100k | wc -l `
* `find / -type f -size +100k -size -5M | wc -l`
* `find / -type f -size +100k -size -5M -exec cp {} /home/dt/Desktop/copy_here \;`
* `find . -type f -name "neddle.txt"`
* `find . -type f -name "neddle.txt -exec mv {} /home/dt/Desktop \;"`

---

**Viewing Files**

* 5 new commands to maipulate file contents.

* `cat file1.txt`
* `tac file1.txt`
* `rev file1.txt`
* `less file1.txt`
* `cat file1.txt | head -n 2`
* `cat file1.txt | tail`

---

**Sorting Data**

* How to sort files and data using the *`sort`* command.

* `sort words.txt | tac`
* `sort -r words.txt` -r mean this --reverse reverse the result of comparisons
* `sort -r words.txt | less`
* `sort -nr numbers.txt | less`  -n mean this  --numeric-sort compare according to string numerical value
* `sort -u numbers.txt | less` -u --unique 
* `ls -la /etc | head -n 20 | sort -k 5n` -k, --key=KEYDEF sort via a key; KEYDEF gives location and type

---

**Searching File Content**

* How to search through files and standard output using *`grep`*.

* `grep e words.txt`
* `grep -c -i e words.txt`
* `ls -lF / | grep root`
* `ls -F /etc | grep -v / > files.txt`

---

**File Archiving + Compression**

* How to *`Archive`* and *`Compress`* files in linux.

* `tar -cvf ourarchive.tar file[1-3].txt` -c, --create create a new archive, -v, --verbose verbosely list files processed, -f, --file=ARCHIVE use archive file or device ARCHIVE
* `tar -xvf ourarchive.tar`
* `gzip ourarchive.tar`
* `gunzip ourarchive.tar.gz`
* `bzip2 ourarchive.tar`
* `bunzip2 ourarchive.tar.bz2`
* `zip ourthing.zip file.txt`
* `unzip ourthing.zip`
* `tar -cvzf ourarchive.tar.gz file[1-3].txt` 
* `tar -cvjf ourarchive.tar.bz2 file[1-3].txt` 