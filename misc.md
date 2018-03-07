# Misc Commands

These are useful commandline programs, but are small enough to not require a whole notes page.

## Redirection & Double-Redirection

```
$ pwd > current_dir
$ cat current_dir
/Users/harrisonturton/Desktop

$ echo hi > current_dir
$ cat current_dir
hi
```

Redirection takes the stdout and puts it into a new file. If the file already exists, it is overwritten.

```
pwd >> current_directory.txt
```

Double-redirection takes the stdour and puts it into a new file. If the file already exists, it is appended.

```
$ echo one >> test.txt
$ echo two >> test.txt
$ cat test
one
two
```

## Piping

```
ls | head -n 3 > first_three_files
```

Piping funnels the stdout and passes it to another utility.

## Grep

```
grep "pattern" <filename>
```

* `(-B | --before-context) <int>` to display `<int>` lines of context before the match
* `(-A | --after-context) <int>` to display `<int>` lines of context after the match
* `(-C | --context) <int>` to display `<int>` lines of context before & after the match

If `grep` is too slow, use `fgrep` \(fixed grep\). It does not support regular expressions.

#### Search within subdirectories

```
grep -r "regex pattern" .
```

#### Piped

```
cat <filename> | grep "regex pattern"
```

## Find

```
find . -name <filename regex>
```

* `.` Searches under the current directory
* `-name` searches through names

e.g. `find . -name *.go` to find all the go files underneath the current directory

## Processes

**List Processes**

```
ps -e
```

**Kill Processes**

```
kill -s <PID>
```


## Sed

```
sed "s/match/replacement/g" <filename>
```

Note that `sed` does not edit the file in-place, but returns the changes \(ready to be piped or redirected\).

```
sed "s/match/replacement/g" <filename> > <new-filename>
```

To **edit the file in-place** \(dangerous!\) use `sed -i`.

