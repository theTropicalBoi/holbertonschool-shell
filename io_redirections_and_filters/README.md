#I/O Redirections & Filters

## Overview of Key Concepts

### 1. Shell and I/O Redirection

- **Standard Input (stdin)**: The default source of input, usually the keyboard.
- **Standard Output (stdout)**: The default destination for output, typically the terminal.
- **Standard Error (stderr)**: The destination for error messages, usually the terminal.
#### Redirection operators:
- `>`: Redirect stdout to a file (overwrites the file).
- `>>`: Append stdout to a file (does not overwrite the file).
- `<`: Redirect stdin from a file.
- `2>`: Redirect stderr to a file.
- `|` (pipe): Sends the output of one command as input to another command.

### 2. Common Shell Commands
- **`echo`**: Displays a line of text.
- **`cat`**: Concatenates and displays files.
- **`head`**: Displays the first few lines of a file.
- **`tail`**: Displays the last few lines of a file.
- **`find`**: Searches for files in a directory hierarchy.
- **`wc`**: Word count, it counts lines, words, and bytes in files.
- **`sort`**: Sorts lines of text files.
- **`uniq`**: Filters out repeated lines.
- **`grep`**: Searches for patterns in files.
- **`tr`**: Translates or deletes characters.
- **`rev`**: Reverses the order of characters in each line.
- **`cut`**: Removes sections from each line of files.
### 3. Special Characters in Bash
- **Whitespace**: Used to separate commands and arguments.
- **Single quotes (`'`)**: Preserve the literal value of characters inside the quotes.
- **Double quotes (`"`)**: Allow for variable expansion inside the quotes.
- **Backslash (`\`)**: Escapes the special meaning of a character.
- **Comment (`#`)**: Used to write comments in scripts.
- **Pipe (`|`)**: Sends the output of one command to another as input.
- **Command separator (`;`)**: Used to execute multiple commands on a single line.
- **Tilde (`~`)**: Represents the home directory.

### 4. Files: `/etc/passwd` and `/etc/shadow`
- **`/etc/passwd`**: Contains user account information. Each line represents a user, with fields like username, user ID (UID), group ID (GID), home directory, and shell.
- **`/etc/shadow`**: Stores password hashes and account aging information. Only accessible by the root user.


1. **What do the commands `head`, `tail`, `find`, `wc`, `sort`, `uniq`, `grep`, `tr`, `rev`, `cut` do?**
    These are powerful tools for manipulating text and files. You should understand:
    - How to use these commands.
    - Their most common options.
    I can explain or guide you through the use of any of these commands if you need.
2. **How to redirect standard output to a file**
    - Example:
        bash
        Copy code
        `echo "Hello World" > output.txt`
        This will write "Hello World" to the `output.txt` file.
3. **How to get standard input from a file instead of the keyboard**
    - Example:
        bash
        Copy code
        `wc < input.txt`
        This reads the contents of `input.txt` as input for the `wc` (word count) command.
4. **How to send the output from one program to the input of another program**
    - Example:
        bash
        Copy code
        `ls | grep ".txt"`
        This sends the output of the `ls` command to `grep`, which searches for `.txt` files.
5. **How to combine commands and filters with redirections**
    - Example:
        bash
        Copy code
        `cat input.txt | sort | uniq > sorted_unique.txt`
        This reads `input.txt`, sorts it, removes duplicates, and saves the result in `sorted_unique.txt`.
6. **Special Characters in Bash**
    - Understanding special characters like `|`, `>`, `<`, `;`, and quoting rules (`'`, `"`) is crucial when writing shell scripts.
 
