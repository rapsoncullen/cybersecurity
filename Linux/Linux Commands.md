## ls
	- Gives the name of every file in the Working Directory
	- All Commands Given
		- -a, --all                  do not ignore entries starting with .
			  -A, --almost-all           do not list implied . and ..
				  --author               with -l, print the author of each file
			  -b, --escape               print C-style escapes for nongraphic characters
				  --block-size=SIZE      with -l, scale sizes by SIZE when printing them;
										   e.g., '--block-size=M'; see SIZE format below
			  -B, --ignore-backups       do not list implied entries ending with ~
			  -c                         with -lt: sort by, and show, ctime (time of last
										   modification of file status information);
										   with -l: show ctime and sort by name;
										   otherwise: sort by ctime, newest first
			  -C                         list entries by columns
				  --color[=WHEN]         colorize the output; WHEN can be 'always' (default
										   if omitted), 'auto', or 'never'; more info below
			  -d, --directory            list directories themselves, not their contents
			  -D, --dired                generate output designed for Emacs' dired mode
			  -f                         do not sort, enable -aU, disable -ls --color
			  -F, --classify             append indicator (one of */=>@|) to entries
				  --file-type            likewise, except do not append '*'
				  --format=WORD          across -x, commas -m, horizontal -x, long -l,
										   single-column -1, verbose -l, vertical -C
				  --full-time            like -l --time-style=full-iso
			  -g                         like -l, but do not list owner
				  --group-directories-first
										 group directories before files;
										   can be augmented with a --sort option, but any
										   use of --sort=none (-U) disables grouping
			  -G, --no-group             in a long listing, don't print group names
			  -h, --human-readable       with -l and -s, print sizes like 1K 234M 2G etc.
				  --si                   likewise, but use powers of 1000 not 1024
			  -H, --dereference-command-line
										 follow symbolic links listed on the command line
				  --dereference-command-line-symlink-to-dir
										 follow each command line symbolic link
										   that points to a directory
				  --hide=PATTERN         do not list implied entries matching shell PATTERN
										   (overridden by -a or -A)
				  --hyperlink[=WHEN]     hyperlink file names; WHEN can be 'always'
										   (default if omitted), 'auto', or 'never'
				  --indicator-style=WORD  append indicator with style WORD to entry names:
										   none (default), slash (-p),
										   file-type (--file-type), classify (-F)
			  -i, --inode                print the index number of each file
			  -I, --ignore=PATTERN       do not list implied entries matching shell PATTERN
			  -k, --kibibytes            default to 1024-byte blocks for disk usage;
										   used only with -s and per directory totals
			  -l                         use a long listing format
			  -L, --dereference          when showing file information for a symbolic
										   link, show information for the file the link
										   references rather than for the link itself
			  -m                         fill width with a comma separated list of entries
			  -n, --numeric-uid-gid      like -l, but list numeric user and group IDs
			  -N, --literal              print entry names without quoting
			  -o                         like -l, but do not list group information
			  -p, --indicator-style=slash
										 append / indicator to directories
			  -q, --hide-control-chars   print ? instead of nongraphic characters
				  --show-control-chars   show nongraphic characters as-is (the default,
										   unless program is 'ls' and output is a terminal)
			  -Q, --quote-name           enclose entry names in double quotes
				  --quoting-style=WORD   use quoting style WORD for entry names:
										   literal, locale, shell, shell-always,
										   shell-escape, shell-escape-always, c, escape
										   (overrides QUOTING_STYLE environment variable)
			  -r, --reverse              reverse order while sorting
			  -R, --recursive            list subdirectories recursively
			  -s, --size                 print the allocated size of each file, in blocks
			  -S                         sort by file size, largest first
				  --sort=WORD            sort by WORD instead of name: none (-U), size (-S),
										   time (-t), version (-v), extension (-X)
				  --time=WORD            change the default of using modification times;
										   access time (-u): atime, access, use;
										   change time (-c): ctime, status;
										   birth time: birth, creation;
										 with -l, WORD determines which time to show;
										 with --sort=time, sort by WORD (newest first)
				  --time-style=TIME_STYLE  time/date format with -l; see TIME_STYLE below
			  -t                         sort by time, newest first; see --time
			  -T, --tabsize=COLS         assume tab stops at each COLS instead of 8
			  -u                         with -lt: sort by, and show, access time;
										   with -l: show access time and sort by name;
										   otherwise: sort by access time, newest first
			  -U                         do not sort; list entries in directory order
			  -v                         natural sort of (version) numbers within text
			  -w, --width=COLS           set output width to COLS.  0 means no limit
			  -x                         list entries by lines instead of by columns
			  -X                         sort alphabetically by entry extension
			  -Z, --context              print any security context of each file
			  -1                         list one file per line.  Avoid '\n' with -q or -b
				  --help     display this help and exit
				  --version  output version information and exit
## cat \<file\>
	- Outputs the contents of a file to the terminal
	- All commands given
		- -A, --show-all           equivalent to -vET
			  -b, --number-nonblank    number nonempty output lines, overrides -n
			  -e                       equivalent to -vE
			  -E, --show-ends          display $ at end of each line
			  -n, --number             number all output lines
			  -s, --squeeze-blank      suppress repeated empty output lines
			  -t                       equivalent to -vT
			  -T, --show-tabs          display TAB characters as ^I
			  -u                       (ignored)
			  -v, --show-nonprinting   use ^ and M- notation, except for LFD and TAB
				  --help     display this help and exit
				  --version  output version information and exit
## chown \<owner\>:\<group\> \<file\>
	- Changes the owner and group of a file to the input
	- Can be used without specifying the group
	- All commands given
		- -c, --changes          like verbose but report only when a change is made
			  -f, --silent, --quiet  suppress most error messages
			  -v, --verbose          output a diagnostic for every file processed
				  --dereference      affect the referent of each symbolic link (this is
									 the default), rather than the symbolic link itself
			  -h, --no-dereference   affect symbolic links instead of any referenced file
									 (useful only on systems that can change the
									 ownership of a symlink)
				  --from=CURRENT_OWNER:CURRENT_GROUP
									 change the owner and/or group of each file only if
									 its current owner and/or group match those specified
									 here.  Either may be omitted, in which case a match
									 is not required for the omitted attribute
				  --no-preserve-root  do not treat '/' specially (the default)
				  --preserve-root    fail to operate recursively on '/'
				  --reference=RFILE  use RFILE's owner and group rather than
									 specifying OWNER:GROUP values
			  -R, --recursive        operate on files and directories recursively

			The following options modify how a hierarchy is traversed when the -R
			option is also specified.  If more than one is specified, only the final
			one takes effect.

			  -H                     if a command line argument is a symbolic link
									 to a directory, traverse it
			  -L                     traverse every symbolic link to a directory
									 encountered
			  -P                     do not traverse any symbolic links (default)
## touch \<file\>
	- Creates a new file
	- All commands given
		- -a                     change only the access time
			  -c, --no-create        do not create any files
			  -d, --date=STRING      parse STRING and use it instead of current time
			  -f                     (ignored)
			  -h, --no-dereference   affect each symbolic link instead of any referenced
									 file (useful only on systems that can change the
									 timestamps of a symlink)
			  -m                     change only the modification time
			  -r, --reference=FILE   use this file's times instead of current time
			  -t STAMP               use [[CC]YY]MMDDhhmm[.ss] instead of current time
				  --time=WORD        change the specified time:
									   WORD is access, atime, or use: equivalent to -a
									   WORD is modify or mtime: equivalent to -m
				  --help     display this help and exit
				  --version  output version information and exit
## su \<user\>
	- Switch to a different user, will require a password if applicable
	- All commands given
		-  -m, -p, --preserve-environment      do not reset environment variables
				 -w, --whitelist-environment <list>  don't reset specified variables

				 -g, --group <group>             specify the primary group
				 -G, --supp-group <group>        specify a supplemental group

				 -, -l, --login                  make the shell a login shell
				 -c, --command <command>         pass a single command to the shell with -c
				 --session-command <command>     pass a single command to the shell with -c
												   and do not create a new session
				 -f, --fast                      pass -f to the shell (for csh or tcsh)
				 -s, --shell <shell>             run <shell> if /etc/shells allows it
				 -P, --pty                       create a new pseudo-terminal

				 -h, --help                      display this help
				 -V, --version                   display version
## ln \<source\> 
	- ln creates links between files. This is mostly used if you need the same file in multiple locations, say if you wanted a file in your python project for it to edit but you also need that file in a seperate program's file.
	- Links between files can either be hard links (actual copies that change with eachother) or symbolic links (a reference to a file)
	- All commands given
		--backup[=CONTROL]
				  make a backup of each existing destination file

		   -b     like --backup but does not accept an argument

		   -d, -F, --directory
				  allow the superuser to attempt to hard link directories (note: will probably fail due to system restrictions, even for the superuser)

		   -f, --force
				  remove existing destination files

		   -i, --interactive
				  prompt whether to remove destinations

		   -L, --logical
				  dereference TARGETs that are symbolic links

		   -n, --no-dereference
				  treat LINK_NAME as a normal file if it is a symbolic link to a directory

		   -P, --physical
				  make hard links directly to symbolic links

		   -r, --relative
				  create symbolic links relative to link location

		   -s, --symbolic
				  make symbolic links instead of hard links

		   -S, --suffix=SUFFIX
				  override the usual backup suffix

		   -t, --target-directory=DIRECTORY
				  specify the DIRECTORY in which to create the links

		   -T, --no-target-directory
				  treat LINK_NAME as a normal file always

		   -v, --verbose
				  print name of each linked file

## find 
	- Find is a powerful tool that allows you to find all files in a directory with a certain attribute such as name, type or permissions, including searching through directories in the directory given.
	- All commands given
		
		-P     Never follow symbolic links.  This is the default behaviour.  When find examines or prints information a file, and the file is a symbolic link, the information used shall be taken from the properties of the symbolic
					  link itself.

       -L     Follow symbolic links.  When find examines or prints information about files, the information used shall be taken from the properties of the file to which the link points, not from the link itself (unless  it  is  a
              broken  symbolic  link  or find is unable to examine the file to which the link points).  Use of this option implies -noleaf.  If you later use the -P option, -noleaf will still be in effect.  If -L is in effect and
              find discovers a symbolic link to a subdirectory during its search, the subdirectory pointed to by the symbolic link will be searched.

              When the -L option is in effect, the -type predicate will always match against the type of the file that a symbolic link points to rather than the link itself (unless the symbolic link is broken).  Actions that  can
              cause symbolic links to become broken while find is executing (for example -delete) can give rise to confusing behaviour.  Using -L causes the -lname and -ilname predicates always to return false.

       -H     Do  not  follow symbolic links, except while processing the command line arguments.  When find examines or prints information about files, the information used shall be taken from the properties of the symbolic link
              itself.  The only exception to this behaviour is when a file specified on the command line is a symbolic link, and the link can be resolved.  For that situation, the information used is taken from whatever the  link
              points to (that is, the link is followed).  The information about the link itself is used as a fallback if the file pointed to by the symbolic link cannot be examined.  If -H is in effect and one of the paths speci‐
              fied on the command line is a symbolic link to a directory, the contents of that directory will be examined (though of course -maxdepth 0 would prevent this).

       If more than one of -H, -L and -P is specified, each overrides the others; the last one appearing on the command line takes effect.  Since it is the default, the -P option should be considered to be in effect unless either
       -H or -L is specified.

       GNU  find  frequently  stats  files during the processing of the command line itself, before any searching has begun.  These options also affect how those arguments are processed.  Specifically, there are a number of tests
       that compare files listed on the command line against a file we are currently considering.  In each case, the file specified on the command line will have been examined and some of its properties will have been saved.   If
       the  named  file  is in fact a symbolic link, and the -P option is in effect (or if neither -H nor -L were specified), the information used for the comparison will be taken from the properties of the symbolic link.  Other‐
       wise, it will be taken from the properties of the file the link points to.  If find cannot follow the link (for example because it has insufficient privileges or the link points to a nonexistent file) the properties of the
       link itself will be used.

       When  the  -H  or -L options are in effect, any symbolic links listed as the argument of -newer will be dereferenced, and the timestamp will be taken from the file to which the symbolic link points.  The same consideration
       applies to -newerXY, -anewer and -cnewer.

       The -follow option has a similar effect to -L, though it takes effect at the point where it appears (that is, if -L is not used but -follow is, any symbolic links appearing after -follow on the command line will be  deref‐
       erenced, and those before it will not).

       -D debugopts
              Print diagnostic information; this can be helpful to diagnose problems with why find is not doing what you want.  The list of debug options should be comma separated.  Compatibility of the debug options is not guar‐
              anteed between releases of findutils.  For a complete list of valid debug options, see the output of find -D help.  Valid debug options include

              exec   Show diagnostic information relating to -exec, -execdir, -ok and -okdir

              opt    Prints diagnostic information relating to the optimisation of the expression tree; see the -O option.

              rates  Prints a summary indicating how often each predicate succeeded or failed.

              search Navigate the directory tree verbosely.

              stat   Print messages as files are examined with the stat and lstat system calls.  The find program tries to minimise such calls.

              tree   Show the expression tree in its original and optimised form.

              all    Enable all of the other debug options (but help).

## grep
	- grep is used to find all strings of a given regex in a file.
	- All commands given
		  -E, --extended-regexp     PATTERNS are extended regular expressions
		  -F, --fixed-strings       PATTERNS are strings
		  -G, --basic-regexp        PATTERNS are basic regular expressions
		  -P, --perl-regexp         PATTERNS are Perl regular expressions
		  -e, --regexp=PATTERNS     use PATTERNS for matching
		  -f, --file=FILE           take PATTERNS from FILE
		  -i, --ignore-case         ignore case distinctions in patterns and data
			  --no-ignore-case      do not ignore case distinctions (default)
		  -w, --word-regexp         match only whole words
		  -x, --line-regexp         match only whole lines
		  -z, --null-data           a data line ends in 0 byte, not newline

		Miscellaneous:
		  -s, --no-messages         suppress error messages
		  -v, --invert-match        select non-matching lines
		  -V, --version             display version information and exit
			  --help                display this help text and exit

		Output control:
		  -m, --max-count=NUM       stop after NUM selected lines
		  -b, --byte-offset         print the byte offset with output lines
		  -n, --line-number         print line number with output lines
			  --line-buffered       flush output on every line
		  -H, --with-filename       print file name with output lines
		  -h, --no-filename         suppress the file name prefix on output
			  --label=LABEL         use LABEL as the standard input file name prefix
		  -o, --only-matching       show only nonempty parts of lines that match
		  -q, --quiet, --silent     suppress all normal output
			  --binary-files=TYPE   assume that binary files are TYPE;
									TYPE is 'binary', 'text', or 'without-match'
		  -a, --text                equivalent to --binary-files=text
		  -I                        equivalent to --binary-files=without-match
		  -d, --directories=ACTION  how to handle directories;
									ACTION is 'read', 'recurse', or 'skip'
		  -D, --devices=ACTION      how to handle devices, FIFOs and sockets;
									ACTION is 'read' or 'skip'
		  -r, --recursive           like --directories=recurse
		  -R, --dereference-recursive  likewise, but follow all symlinks
			  --include=GLOB        search only files that match GLOB (a file pattern)
			  --exclude=GLOB        skip files that match GLOB
			  --exclude-from=FILE   skip files that match any file pattern from FILE
			  --exclude-dir=GLOB    skip directories that match GLOB
		  -L, --files-without-match  print only names of FILEs with no selected lines
		  -l, --files-with-matches  print only names of FILEs with selected lines
		  -c, --count               print only a count of selected lines per FILE
		  -T, --initial-tab         make tabs line up (if needed)
		  -Z, --null                print 0 byte after FILE name

		Context control:
		  -B, --before-context=NUM  print NUM lines of leading context
		  -A, --after-context=NUM   print NUM lines of trailing context
		  -C, --context=NUM         print NUM lines of output context
		  -NUM                      same as --context=NUM
			  --color[=WHEN],
			  --colour[=WHEN]       use markers to highlight the matching strings;
									WHEN is 'always', 'never', or 'auto'
		  -U, --binary              do not strip CR characters at EOL (MSDOS/Windows)
## diff
	- The diff command is used for finding differences between files in linux
	- All commands given
		--normal
              output a normal diff (the default)

       -q, --brief
              report only when files differ

       -s, --report-identical-files
              report when two files are the same

       -c, -C NUM, --context[=NUM]
              output NUM (default 3) lines of copied context

       -u, -U NUM, --unified[=NUM]
              output NUM (default 3) lines of unified context

       -e, --ed
              output an ed script

       -n, --rcs
              output an RCS format diff

       -y, --side-by-side
              output in two columns

       -W, --width=NUM
              output at most NUM (default 130) print columns

       --left-column
              output only the left column of common lines

       --suppress-common-lines
              do not output common lines

       -p, --show-c-function
              show which C function each change is in

       -F, --show-function-line=RE
              show the most recent line matching RE

       --label LABEL
              use LABEL instead of file name and timestamp (can be repeated)

       -t, --expand-tabs
              expand tabs to spaces in output

       -T, --initial-tab
              make tabs line up by prepending a tab

       --tabsize=NUM
              tab stops every NUM (default 8) print columns

       --suppress-blank-empty
              suppress space or tab before empty output lines

       -l, --paginate
              pass output through 'pr' to paginate it
		-r, --recursive
              recursively compare any subdirectories found

       --no-dereference
              don't follow symbolic links

       -N, --new-file
              treat absent files as empty

       --unidirectional-new-file
              treat absent first files as empty

       --ignore-file-name-case
              ignore case when comparing file names

       --no-ignore-file-name-case
              consider case when comparing file names

       -x, --exclude=PAT
              exclude files that match PAT

       -X, --exclude-from=FILE
              exclude files that match any pattern in FILE

       -S, --starting-file=FILE
              start with FILE when comparing directories

       --from-file=FILE1
              compare FILE1 to all operands; FILE1 can be a directory

       --to-file=FILE2
              compare all operands to FILE2; FILE2 can be a directory

       -i, --ignore-case
              ignore case differences in file contents

       -E, --ignore-tab-expansion
              ignore changes due to tab expansion

       -Z, --ignore-trailing-space
              ignore white space at line end

       -b, --ignore-space-change
              ignore changes in the amount of white space

       -w, --ignore-all-space
              ignore all white space

       -B, --ignore-blank-lines
              ignore changes where lines are all blank

       -I, --ignore-matching-lines=RE
              ignore changes where all lines match RE

       -a, --text
              treat all files as text
## clang
	- clang is used to run C files with the syntax clang <filename.c>
	- Common tags
		- -o <name>
			- Lets you name your runnable file
## which
	- Tells you which file would be run if you were to use the command supplied with the context which <command>