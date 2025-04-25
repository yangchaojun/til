A mark is set to any cursor location using the `m` command.

For examples:
`ma` is set `a` mark, `mz` is set `z` mark

# Jump to marks

jump to the start of the line

```vim
'{a-z}
```

jump to the precise location of mark

```vim
`{a-z}
```

# viem all marks

```vim
:marks
```
# clear the marks

```vim 
:delmarks a

:delmarks a-z
```