# prompt_maker
Python script to generates bash PS1 prompts using template blocks

## Usage
`prompt_maker [-h] "<string>"`

Where `<string>` refers to any combination of the predefined `[colors]` and `[special]` blocks (enclosed in square brackets), along with any regular characters, including other special characters that bash recognises but aren't listed below.

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
`[bcolors]` are bold colors. `[lbracket]` and `[rbracket]` can be used to insert literal `[` and `]` respectively.

### Example:
`prompt_maker "[red][username]@[hostshort]:[bgreen][dirfull][nocolor][dollar]"`

becomes

`PS1='\[\e[0;31m\]\u@\h:\[\e[1;32m\]\w\[\e[m\]\$ \[\e[m\]'`

![image](https://user-images.githubusercontent.com/29720696/187603729-5585f543-eeb3-4dda-99fe-0308b4e48ad0.png)

