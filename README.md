# Code Problem Format Standard ![Version Badge](https://img.shields.io/github/release/zebMcCorkle/code-problem-format.svg?style=flat-square)

The two main parts of this spec:

 1. The file must be fully compatible with YAML
 2. The file must be human-readable

## File layout

### Example file

```YAML
title: Crawl
languages:
  - Java
filename: Crawl.java
overview: "Write a program that prints the exact content of the input file. Note that this should ***not*** be hard coded. **We will check.**"
input: None.
output: The contents of `crawl.dat`
cases:
  - files:
      crawl.dat: "\"It is a period of civil war. Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire. During the battle, rebel spies managed to steal secret plans to the Empire's ultimate weapon, the DEATH STAR, an armored space station with enough power to destroy an entire planet. Pursued by the Empire's sinister agents, Princess Leia races home aboard her starship, custodian of the stolen plans that can save her people and restore freedom to the galaxy....\""
    stdin: ""
    stdout: "\"It is a period of civil war. Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire. During the battle, rebel spies managed to steal secret plans to the Empire's ultimate weapon, the DEATH STAR, an armored space station with enough power to destroy an entire planet. Pursued by the Empire's sinister agents, Princess Leia races home aboard her starship, custodian of the stolen plans that can save her people and restore freedom to the galaxy....\""
```

#### Example output

> | Name        | Crawl                                                                                                                              |
> |-------------|------------------------------------------------------------------------------------------------------------------------------------|
> | Language    | Java                                                                                                                               |
> | Description | Write a program that prints the exact content of the input file. Note that this should ***not*** be hard coded. **We will check.** |
> | Input       | None.                                                                                                                              |
> | Output      | The contents of `crawl.dat`                                                                                                        |                                                                                                     
> 
> ## Example test case
> 
> `crawl.dat`: "It is a period of civil war. Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire. During the battle, rebel spies managed to steal secret plans to the Empire's ultimate weapon, the DEATH STAR, an armored space station with enough power to destroy an entire planet. Pursued by the Empire's sinister agents, Princess Leia races home aboard her starship, custodian of the stolen plans that can save her people and restore freedom to the galaxy...."
> 
> ---
> 
> `stdin`:
> 
> ---
> 
> `stdout`: "It is a period of civil war. Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire. During the battle, rebel spies managed to steal secret plans to the Empire's ultimate weapon, the DEATH STAR, an armored space station with enough power to destroy an entire planet. Pursued by the Empire's sinister agents, Princess Leia races home aboard her starship, custodian of the stolen plans that can save her people and restore freedom to the galaxy...."

### Fields

#### Title

`string`: contains the name of the code problem

#### Languages

`string[]`: contains the list of usable languages

#### Filename

`string`: name of the file the code will be placed in

#### Overview

`string`: description of the problem in Markdown

#### Input

`string`: description of the input in Markdown

#### Output

`string`: description of the output in Markdown

#### Cases

`case[]`: contains all of the test cases for the problem

### Type definitions

#### `type[]`: array of `type`

#### `typea:typeb`: map of `typeb` with `typea` as keys

#### `string`: a string of characters

#### `case`: an object containing the following:

##### Files

`string:string`: contains the contents of any auxiliary files for the problem

##### STDIN

`string`: data to be piped into `stdin`

##### STDOUT

`string`: data to be expected from `stdout`
