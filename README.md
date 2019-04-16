# prompt_maker
Create bash PS1 prompt using template blocks

## Usage
`usage: prompt_maker [-h] "<string>"`

Where `<string>` can be any combination of the predefined `[colors]` and `[special]` blocks
enclosed in square brackets, along with any regular characters, including the
more complex special characters that bash recognises but aren't listed below.

### Templates:
```
colors:                 special:
[black]                 [username]
[red]                   [hostshort]
[green]                 [hostfull]
[yellow]                [dirshort]
[blue]                  [dirfull]
[purple]                [newline]
[cyan]                  [date]
[white]                 [time24]
[bblack]                [time12]
[bred]                  [tty]
[bgreen]                [jobs]
[byellow]               [rbracket]
[bblue]                 [lbracket]
[bpurple]               [dollar]
[bcyan]
[bwhite]
[nocolor]
```

### Example:
`prompt_maker "[red][username]@[hostshort]:[bgreen][dirfull][nocolor][dollar]"`

becomes

`PS1='\[\e[0;31m\]\u@\h:\[\e[1;32m\]\w\[\e[m\]\$ \[\e[m\]'`
