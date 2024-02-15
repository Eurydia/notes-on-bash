# Basic shell features

Summarized from [Basic shell features](https://www.gnu.org/software/bash/manual/bash.html#Basic-Shell-Features).

## Syntax

When given an input, a shell tokenizes it into **words** and **operators**. Then, it parses the tokens into commands and other constructs. The commands are executed and their **exit statuses** are returned.

If the shell encounters the beginning of a comment (**#**), the hsell ignores the hashtag symbol and the rest of that line.

### Shell operation

More specifially, a shell performs the following steps; (1) reads input from a file or from the terminal, (2) breaks input into tokens, which consists of words and symbols. These tokens are separated at a **metacharacter**, (3) parses the tokens into commands. (4) Performs the shell expansions, (5) performs redirections and removes the redirection operators and their operands from the argument list, (6) executes the commands, (7) waits and collects the commands' exit statuses.

### Quoting

Quoting removes the special meaning of characters, such as **metacharacters**, and **operators**.

There are three quoting mechanisms: the **escape character**, **single quotes**, and **double quotes**.

#### Escape character

A non-quoted backslash (**\\**) is the Bash escape character. It preserves the literal value of the next character that follows, with the exception of **newline**.

When a **newline** is escaped, it is removed from the input, and the two lines are joined together.

#### Single quotes

Characters placed between a pair of single quotes (**'**) loses all of their special meaning. As such a single quote cannot appear in a single-quoted string, even when preceded by a backslash

#### Double quotes

Characters placed between a pair of double quotes (**"**) loses their special meaning, with the exception of **\$**, **\`**, **\\**, and, when history expansion is enabled, **!**.

The characters **\*** and **@** have special meaning when in double quotes.

The backslash retains its special meaning only when followed by one of the following characters: **\$**, **\`**, **"**, **\\**, or **newline**. Backslashes preceding characters without a special meaning do not do anything.
Within double quotes, backslashes that are followed by one of these characters are removed.

A double quote may be quoted within double quotes by escaping it.

#### ANSI-C quoting

Prefixing a single-quoted string with a dollar sign (**\$**), such as **\$'Hi'**, triggers a special kind of single-quoted string. Additional escapable characters are as per specified by ANSI-C standard. These are:

**\\a**

alert (bell)

**\\b**

backspace

**\\e** and **\\E**

an escape character (not ANSI C)

**\\f**

form feed

**\\n**

newline

**\\r**

carriage return

**\\t**

horizontal tab

**\\v**

vertical tab

**\\\\**

backslash

**\\'**

single quote

**\\"**

double quote

**\\?**

question mark

**\\nnn**

the eight-bit character whose value is the octal value **nnn** (one to three octal digits)

**\\xHH**

the eight-bit character whose value is the hexadecimal value **HH** (one or two hex digits)

**\\uHHHH**

the Unicode (ISO/IEC 10646) character whose value is the hexadecimal value **HHHH** (one to four hex digits)

**\\UHHHHHHHH**

the Unicode (ISO/IEC 10646) character whose value is the hexadecimal value **HHHHHHHH** (one to eight hex digits)

**\\cx**

a control-x character

#### Locale-specific translation

Prefixing a double-quoted string with a dollar sign (**\$**), such as **\$"Hello, world"**, translates it according to the current locale.

### Comments
