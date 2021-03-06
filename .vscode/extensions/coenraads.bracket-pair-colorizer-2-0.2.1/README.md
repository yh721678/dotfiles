
---

Note:   
This extension is unmaintained, check out these similar alternatives:  
- [Highlight Matching Tag](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag)  
- [Blockman](https://marketplace.visualstudio.com/items?itemName=leodevbro.blockman)

---

# Bracket Pair Colorizer 2

This extension allows matching brackets to be identified with colours. The user can define which tokens to match, and which colours to use.

Screenshot:  
![Screenshot](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/example.png "Bracket Pair Colorizer")

---

### F.A.Q. 

- Differences between v1 and v2?
    - v2 Uses the same bracket parsing engine as VSCode, greatly increasing speed and accuracy. A new version was released because settings were cleaned up, breaking backwards compatibility.

---

### [Release Notes](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/blob/HEAD/CHANGELOG.md)

---

## Settings

> `"bracket-pair-colorizer-2.colors"`  
Define the colors used to colorize brackets. Accepts valid color names, hex codes, and `rgba()` values.
```json
"bracket-pair-colorizer-2.colors": [
    "Gold",
    "Orchid",
    "LightSkyBlue"
]
```

> `"bracket-pair-colorizer-2.forceUniqueOpeningColor"`  
![Disabled](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/forceUniqueOpeningColorDisabled.png "forceUniqueOpeningColor Disabled")
![Enabled](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/forceUniqueOpeningColorEnabled.png "forceUniqueOpeningColor Enabled")

> `"bracket-pair-colorizer-2.forceIterationColorCycle"`  
![Enabled](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/forceIterationColorCycleEnabled.png "forceIterationColorCycle Enabled")

>`"bracket-pair-colorizer-2.colorMode"`  
Consecutive brackets share a color pool for all bracket types  
Independent brackets allow each bracket type to use its own color pool  
![Consecutive](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/consecutiveExample.png "Consecutive Example")
![Independent](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/independentExample.png "Independent Example")

> `"bracket-pair-colorizer-2.highlightActiveScope"`  
Should the currently scoped brackets always be highlighted?

> `"bracket-pair-colorizer-2.activeScopeCSS"`  
Choose a border style to highlight the active scope. Use `{color}` to match the existing bracket color  
It is recommended to disable the inbuilt `editor.matchBrackets` setting if using this feature  
![BorderStyle](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/activeScopeBorder.png "Active Scope Border Example")  

```json
"bracket-pair-colorizer-2.activeScopeCSS": [
    "borderStyle : solid",
    "borderWidth : 1px",
    "borderColor : {color}",
    "opacity: 0.5"
]
```

> `"bracket-pair-colorizer-2.showBracketsInGutter"`  
> Show active scope brackets in the gutter  
![Gutter](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/gutter.png "Gutter Brackets Example") 

> `"bracket-pair-colorizer-2.showBracketsInRuler"`  
> Show active scope brackets in the ruler  

> `"bracket-pair-colorizer-2.rulerPosition"`  
> Decoration position in the ruler

>`"bracket-pair-colorizer-2.showVerticalScopeLine"`  
Show a vertical line between the brackets?  Enabled by default   
![Scope Line](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/no-extra.png "Gutter Brackets Example")  

>`"bracket-pair-colorizer-2.showHorizontalScopeLine"`  
Show a horizontal line between the brackets? Enabled by default   
![Scope Line](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/extra.png "Gutter Brackets Example")  

>`"bracket-pair-colorizer-2.scopeLineRelativePosition"`  
Disable this to show the vertical line in column 0  
![Scope Line](https://github.com/CoenraadS/Bracket-Pair-Colorizer-2/raw/HEAD/images/no-relative.png "Gutter Brackets Example")  
  
>`"bracket-pair-colorizer-2.scopeLineCSS"`  
Choose a border style to highlight the active scope. Use `{color}` to match the existing bracket color 

```json
"bracket-pair-colorizer-2.scopeLineCSS": [
    "borderStyle : solid",
    "borderWidth : 1px",
    "borderColor : {color}",
    "opacity: 0.5"
]
```

>`"bracket-pair-colorizer-2.excludedLanguages"`  
Exclude a language from being colorized

### Commands

These commands will expand/undo the cursor selection to the next scope

`"bracket-pair-colorizer-2.expandBracketSelection"`  
`"bracket-pair-colorizer-2.undoBracketSelection"`

Quick-start:

```
{
    "key": "shift+alt+right",
    "command": "bracket-pair-colorizer-2.expandBracketSelection",
    "when": "editorTextFocus"
},
{
    "key": "shift+alt+left",
    "command": "bracket-pair-colorizer-2.undoBracketSelection",
    "when": "editorTextFocus"
}
```
