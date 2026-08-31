# Week One Assignment: Set up your system and demonstrate basic UNIX command line actions


**2. Install an AI ready code editor as described on the page. Mention in you README the editor you chose.**

I chose Visual Studio Code

<br>
<br>

**6. What version is your ``samtools`` command in the ``bioinfo`` environment?**

First, enter the working directory for the BMMB 852 class.
 
```
cd ~/edu/bioinfo
```


This will enter the directory, showing:
> brianpraul@MacPraul-Strikes-Again ~/edu/bioinfo

Then, enter the bioinfo environment (after it is set up with Pixi) with:

```
bioinfo
```

Once in the environment, simply type:

```
samtools
```

to get the version and an explanation of the tool (below is truncated to just the version):

> Program: samtools (Tools for alignments in the SAM format)
> Version: 1.24 (using htslib 1.24)

<br>
<br>

**7) Show commands needed to create a nested directory structure.**

After entering the working directory and bioinfo environment, to make a nested directory use the ``mkdir`` command with ``-p``, which will create any parent directories listed if they don't exist. For example:

```
mkdir -p nest1/nest2/nest3
```

Will create the ``nest1`` directory inside ``bioinfo``. ``nest3`` will be within ``nest2`` which in turn is within ``nest1``

<br>
<br>

**8) Show commands that create files in different directories.**

Once you're in the working directory and environment, to make a file in a different directory use the ``touch`` command, like below:

```
touch ~/edu/bioinfo/nested/test.txt
```

This will create a blank test file in the given file path. To change the directory, you can use the following:

```
touch ~/test.txt
```
This makes a text file in your home directory.

```
touch ./test.txt
```
This makes a text file in your current working directory.

```
touch ../test.txt

```
This makes a text file one directory above your current working directory. Assuming I'm currently in ``~/edu/bioinfo``, this command would create ``test.txt`` in ``~/edu``

<br>
<br>


**9) Show how to access these files using relative and absolute paths.**

To use the absolute filepath, use the ``open`` command (if wanting to open the file) or ``cat`` (if you want to view it in the terminal) with the full list of nested directories. It's slower, but you will always pick the right file if the path is specified correctly, regardless of which directory you're in.

```
open /Users/brianpraul/edu/bioinfo/test.txt
```
or, to view in the terminal
```
cat /Users/brianpraul/edu/bioinfo/test.txt
```

For a relative file path, use the ``./`` prefix to reference the current working directory.

```
open ./test.txt
```
or, to view in the terminal
```
cat ./test.txt
```

For another relative file path, use the ``../`` prefix to go one folder above the working directory.

```
open ../test.txt
```
or, to view in the terminal
```
cat ../test.txt
```


