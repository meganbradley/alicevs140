---
title: "Options, Text Editor, C#, Advanced"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 947f9d9a-b0f3-408d-9866-d82895bcee31
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Options, Text Editor, C#, Advanced
Use this dialog box to modify the settings for editor formatting, code refactoring, and XML documentation comments for Visual C#. To access this dialog box, click **Options** on the **Tools** menu, expand the **Text Editor** folder, expand **C#**, and then click **Advanced**.  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## Outlining  
 Enter outlining mode when files open  
 When selected, automatically outlines the code file, which creates collapsible blocks of code. The first time a file is opened, #regions blocks and inactive code blocks collapse.  
  
## Editor Help  
 Underline errors in the editor  
 Identifies build errors in code. When this option is selected, wavy underlines appear in colors that have specific meanings:  
  
-   Parse errors are red.  
  
-   Build errors are blue.  
  
-   Build warnings are green.  
  
-   Invalid [Edit and Continue](../vs140/Edit-and-Continue.md) edits are purple.  
  
 Move the pointer over the underlined code segment to see a ToolTip with information about the error.  
  
 Show live semantic errors  
 Identifies certain compile errors without explicit compilation, for example, declaring and using an unknown type or referencing an unknown property.  
  
 Highlight references to symbol under cursor  
 When the cursor is positioned inside a symbol, or when you click a symbol, all the instances of that symbol in the code file are highlighted.  
  
## Refactoring  
 Verify results of refactoring  
 Displays the **Verification Results** dialog box when you try to refactor code that contains build errors, or when refactoring would cause a code reference to bind to something different from its original binding.  
  
 Warn on members with compiler generated references  
 Displays a warning dialog when you try to refactor a member that has the same name as a compiler generated reference.  
  
## XML Documentation Comments  
 Generate XML documentation comments for ///  
 When selected, inserts the <summary\> start and end tags automatically for XML documentation comments after you type the /// comment introduction. For more information about XML documentation, see [Documenting Your Code with XML](../vs140/XML-Documentation-Comments--C#-Programming-Guide-.md).  
  
## Implement Interface  
 Surround generated code with #region  
 Inserts a #region <*interface name*> Member around the methods when Implement Interface or Implement Interface Explicitly is used.  
  
## Organize Usings  
 Place 'System' directives first when sorting usings  
 When selected, `System` using directives appear before other using directives. For more information, see [Sort Usings](../vs140/Sort-Usings.md).  
  
## See Also  
 [Documenting Your Code with XML](../vs140/XML-Documentation-Comments--C#-Programming-Guide-.md)   
 [Setting Language-Specific Editor Options](../vs140/Setting-Language-Specific-Editor-Options.md)   
 [Visual C# IntelliSense](../Topic/Visual%20C%23%20IntelliSense.md)