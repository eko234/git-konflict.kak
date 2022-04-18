# git-konflict


## Suggested mappings

``` kak
plug "eko234/git-konflict.kak" config %{
  declare-user-mode konflict
  map global user K ': enter-user-mode konflict<ret>'
  map global konflict s ': konflict-start<ret>'
  map global konflict j ': konflict-use-mine<ret>'
  map global konflict k ': konflict-use-yours<ret>'
  map global konflict J ': konflict-use-mine-then-yours<ret>'
  map global konflict K ': konflict-use-yours-then-mine<ret>'
  map global konflict d ': konflict-use-none<ret>'
}
```


## Commands

The base commands for `use-mine` and `use-yours` were
taken from the kakoune discuss forum, thanks krobelus!,
I added some more functionalities, the command `konflict-start`
will highlight all blocks with the pattern of a git conflict
and then grep for lines that start with `<<<<<` so you can
navigate conflicts with ease.

![theme image](https://github.com/eko234/git-konflict.kak/blob/main/konflict.gif)

