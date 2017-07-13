# AceEditor
SpiderBasic-Module to use the AceEditor (https://ace.c9.io/)

![http://i.imgur.com/dbCBQw2.png](http://i.imgur.com/dbCBQw2.png)

> Ace is an embeddable code editor written in JavaScript. It matches the features and performance of native editors such as Sublime, Vim and TextMate. It can be easily embedded in any web page and JavaScript application. Ace is maintained as the primary editor for Cloud9 IDE and is the successor of the Mozilla Skywriter (Bespin) project.

# Installation:

Copy `AceEditor.sbi` into a folder of your choice and include this file with XIncludeFile in your source.

```vbs
XIncludeFile "path/to/your/AceEditor.sbi"
```

# Usage:

First you must initialize the module:


```vbs
XIncludeFile "AceEditor.sbi"

EnableExplicit
  
Procedure Main()

    ; here we are!

EndProcedure

AceEditor::Init(@Main())
```

In the Main-Procedure, open a window, create a ContainerGadget and bind the AceEditor to it:

```vbs
[...]

Procedure Main()

    OpenWindow(#Window, ...)
  
    ContainerGadget(#AceEditor, ...)
    CloseGadgetList()

    AceEditor::BindGadget(#AceEditor)

EndProcedure

[...]
```
