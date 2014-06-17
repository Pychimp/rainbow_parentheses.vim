# Better Rainbow Parentheses

### Options:

```vim
let g:rbpt_colorpairs = [
    \ ['brown',       'RoyalBlue3'],
    \ ['Darkblue',    'SeaGreen3'],
    \ ['darkgray',    'DarkOrchid3'],
    \ ['darkgreen',   'firebrick3'],
    \ ['darkcyan',    'RoyalBlue3'],
    \ ['darkred',     'SeaGreen3'],
    \ ['darkmagenta', 'DarkOrchid3'],
    \ ['brown',       'firebrick3'],
    \ ['gray',        'RoyalBlue3'],
    \ ['black',       'SeaGreen3'],
    \ ['darkmagenta', 'DarkOrchid3'],
    \ ['Darkblue',    'firebrick3'],
    \ ['darkgreen',   'RoyalBlue3'],
    \ ['darkcyan',    'SeaGreen3'],
    \ ['darkred',     'DarkOrchid3'],
    \ ['red',         'firebrick3'],
    \ ]
```

```vim
let g:rbpt_max = 16
```

```vim
let g:rbpt_loadcmd_toggle = 0
```

### Commands:

```vim
:RainbowParenthesesToggle       " Toggle it on/off
:RainbowParenthesesLoadRound    " (), the default when toggling
:RainbowParenthesesLoadSquare   " []
:RainbowParenthesesLoadBraces   " {}
:RainbowParenthesesLoadChevrons " <>
```

### Always On:

```vim
au VimEnter * RainbowParenthesesToggle
au Syntax * RainbowParenthesesLoadRound
au Syntax * RainbowParenthesesLoadSquare
au Syntax * RainbowParenthesesLoadBraces
```

---

Most of is taken as from ```kien/rainbow_parentheses.vim```,
these changes make the colours better suited for light colorschemes

###### (Pretty much, WIP !)

```diff
diff --git a/autoload/rainbow_parentheses.vim b/autoload/rainbow_parentheses.vim
index 87a74ad..4bad954 100644
--- a/autoload/rainbow_parentheses.vim
+++ b/autoload/rainbow_parentheses.vim
@@ -5,22 +5,22 @@
 "==============================================================================
 
 let s:pairs = [
-	\ ['brown',       'RoyalBlue3'],
-	\ ['Darkblue',    'SeaGreen3'],
-	\ ['darkgray',    'DarkOrchid3'],
+	\ ['brown',       '#a4c639'],
+	\ ['Darkblue',    '#ffbbbb'],
+	\ ['darkgray',    '#00ff00'],
 	\ ['darkgreen',   'firebrick3'],
 	\ ['darkcyan',    'RoyalBlue3'],
 	\ ['darkred',     'SeaGreen3'],
 	\ ['darkmagenta', 'DarkOrchid3'],
 	\ ['brown',       'firebrick3'],
 	\ ['gray',        'RoyalBlue3'],
-	\ ['black',       'SeaGreen3'],
+	\ ['black',       '#007fff'],
 	\ ['darkmagenta', 'DarkOrchid3'],
 	\ ['Darkblue',    'firebrick3'],
 	\ ['darkgreen',   'RoyalBlue3'],
-	\ ['darkcyan',    'SeaGreen3'],
-	\ ['darkred',     'DarkOrchid3'],
-	\ ['red',         'firebrick3'],
+	\ ['darkcyan',    '#ff0000'],
+	\ ['darkred',     '#eb6300'],
+  \ ['red',         '#078251'],
 	\ ]
 let s:pairs = exists('g:rbpt_colorpairs') ? g:rbpt_colorpairs : s:pairs
 let s:max = exists('g:rbpt_max') ? g:rbpt_max : max([len(s:pairs), 16])
```
