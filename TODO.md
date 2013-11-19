# Next steps

* edit:
    - Highlighting beyond lexer and maybe even parser (highlighting of valid
      and invalid command names a la fish, and valid and invalid variable
      expansions)
    - Multiline editing
* eval:
    - Implement variable capture of closures
    - Adopt the reference/value duality of $a, so that `set a []` is
      written as `set $a []` (like Perl)? Would faciliates variable capture of
      closures
    - Determine namespacing model (importable modules; relationship of
      functions vs. external commands, variables vs. environmental variables)
    - Implement control structures; settle down its syntax - special syntax or
      closure syntax?
    - Determine failing model (boundary of failure; exception handling a la
      Python/Lua/...  and/or error value handling a la golang)
    - Support evaluating script
* eval/builtins
    - Failing, intermediate state:
        ```var ${echo a | tee /tmp/a} b = 1```
      Should arity mismatch be detected early and avoid the side-effect of
      writing `/tmp/a`? Should $a and $b be defined?
* All the TODO and XXX's in source :)