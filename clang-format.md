```bash
clang-format -style=microsoft -dump-config > .clang-format
```

```bash
---
Language: Cpp
BasedOnStyle: Microsoft

# === Indentation & Alignment ===
UseTab: Always
IndentWidth: 4
TabWidth: 4
ContinuationIndentWidth: 4
AccessModifierOffset: -2
AlignAfterOpenBracket: Align
AlignOperands: Align
AlignTrailingComments: true

# === Braces & Blocks ===
BreakBeforeBraces: Attach # void func() {
BraceWrapping:
  AfterFunction: true
  AfterClass: true
  AfterStruct: true
  AfterNamespace: true
  BeforeElse: true
  BeforeCatch: true

# === Line & Spacing ===
ColumnLimit: 120
SpaceBeforeParens: ControlStatements
SpaceBeforeParensOptions:
  AfterControlStatements: true
  AfterFunctionDefinitionName: false
  AfterFunctionDeclarationName: false
PointerAlignment: Right
SpaceAfterTemplateKeyword: true
SpacesInContainerLiterals: true
SpacesInParentheses: false
SpacesInSquareBrackets: false

# === Statements & Formatting Rules ===
AllowShortFunctionsOnASingleLine: None
AllowShortIfStatementsOnASingleLine: Never
AllowShortLoopsOnASingleLine: false
AllowShortBlocksOnASingleLine: Never
AllowShortCaseLabelsOnASingleLine: false
AllowAllParametersOfDeclarationOnNextLine: true
AllowAllArgumentsOnNextLine: true

# === Includes ===
SortIncludes: CaseSensitive
IncludeBlocks: Preserve

# === Misc ===
FixNamespaceComments: true
NamespaceIndentation: None
ReflowComments: true
Standard: Cpp23

---


```