# Definitions

Summarized from [Definitions](https://www.gnu.org/software/bash/manual/bash.html#Definitions)

**control operator**

A sequence of symbol or a token that has special meaning. It is a newline or one of the following: **||**, **&&**, **&**, **;**, **;;**, **;&**, **;;&**, **|**, **|&**, **(**, or **)**.

**exit status** and **return status**

The value returned by a command to its caller. The value is restricted to eight bits from 0 to 255.

**field**

The name of a command being executed or its arguments.

**job**

A set of processes comprising a pipeline, and any processes descended from it, that are all in the same process group.

**job control**

A mechanism by which users can selectively stop (suspend) and restart (resume) execution of processes.

**metacharacter**

A single symbol delimits **fields** or **word**. A metacharacter is a space, tab, newline, or one of the following characters: **|**, **&**, **;**, **(**, **)**, **<**, or **>**.

**operator**

A **control operator** or a **redirection operator**. Operators contain at least one unquoted **metacharacter**.

**process group**

A collection of related processes each having the same process group ID.

**process group ID**

A unique identifier that represents a process group during its lifetime.

**signal**

A mechanism by which a process may be notified by the kernel of an event occurring in the system.

**token**

A sequence of characters considered a single unit by the shell. It is either a **word** or an **operator**.

**word**

A sequence of characters treated as a unit by the shell. Words may not include unquoted metacharacters.
