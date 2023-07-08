# CSS structure

For the global css, we try to stick to the structure of [ITCSS ](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/). Since a lot of the Vue components' styling will go into the .vue files, some of the folders may remain empty. I do prefer keeping the empty folders in place for the sake of clearity.

# CSS class naming

Having component styles inside .vue files also takes away some of the necessity of using BEM, but even if you might not need the block-level, I do like the use of `--` for modifiers. Also, using [prefixes for classes](https://csswizardry.com/2015/03/more-transparent-ui-code-with-namespaces/) can still be useful. At least use those for objects (`o-`) and utilities (`-u`).
