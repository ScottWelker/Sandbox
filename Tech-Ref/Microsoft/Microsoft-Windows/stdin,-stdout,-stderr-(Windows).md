[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Windows](/Tech-Ref/Microsoft/Microsoft-Windows)

[[_TOC_]]

---
# Introduction
"_***stdin, stdout, stderr*** are standard streams for input, output, and error output._"

"_In computer programming, standard streams are interconnected input and output communication channels between a computer program and its environment when it begins execution. The three input/output (I/O) connections are called_ ***standard input (stdin),*** ***standard output (stdout)*** and ***standard error (stderr).*** "

## Reference
1. [Wikipedia: Standard Streams](https://en.wikipedia.org/wiki/Standard_streams)
1. [Docs.Microsoft: stdin, stdout, stderr](https://docs.microsoft.com/en-us/cpp/c-runtime-library/stdin-stdout-stderr?view=msvc-170)

---
# Topics
1. [Command Line Interface (CLI)](/Tech-Ref/CLI-\(Command-Line-Interface\)).
1. [Microsoft Windows](/Tech-Ref/Microsoft/Microsoft-Windows).
1. [Software Development](/Tech-Ref/Software-Development).

---
# Tips and Tricks

## Redirecting Command Prompt stdout/stderr
- [Windows Command Prompt Redirecting STDOUT/STDERR](https://www.rushis.com/windows-command-prompt-redirecting-stdoutstderr/)

### STDERR and STDOUT to Different Files
- `dir nosuchfile.txt > out.log 2>error.log`

### STDERR and STDOUT to Same File
- `dir nosuchfile.txt > alloutput.log 2>&1`

[SWelker](/Individuals/Scott-Welker) real-world use case. [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli) emits the bulk of its meaningful content to `stderr`. For a large input, e.g. a folder full of [Markdown files](/Tech-Ref/Software-Development/Markup-Language/Markdown)), it is sometimes useful to unify the output in a single file for review.

This redirects `stdout` to the file `c:\Temp\KM.txt` and `stderr` into `stdout`. All output then is in the file `c:\Temp\KM.txt`.

```cmd
remark --use remark-validate-links .\ 1>c:\Temp\KM.txt 2>&1
```
