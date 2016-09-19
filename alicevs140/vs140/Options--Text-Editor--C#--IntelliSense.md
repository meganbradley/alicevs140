---
title: "Options, Text Editor, C#, IntelliSense"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3466dedb-e5f4-424c-8dd8-e4941b2f4fc2
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Options, Text Editor, C#, IntelliSense
Use the **IntelliSense** property page to modify settings that affect the behavior of IntelliSense for Visual C#. You can access the **IntelliSense** property page by clicking **Options** on the **Tools** menu, then clicking **C#** in the **Text Editor** folder, and then clicking **IntelliSense.**  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
 The **IntelliSense** property page contains the following properties:  
  
## Completion Lists  
 **Show completion list after a character is typed**  
 When this option is selected, IntelliSense automatically displays the completion list when you begin typing. When this option is not selected, IntelliSense completion is still available from the **IntelliSense** menu or by pressing CTRL+SPACE.  
  
 **Place keywords in completion lists**  
 When this option is selected, IntelliSense adds C# keywords, for example, [class](../vs140/class--C#-Reference-.md), to the completion list.  
  
 **Place code snippets in completion lists**  
 When this option is selected, IntelliSense adds aliases for C# code snippets to the completion list. In the case where the code snippet alias is the same as a keyword, for example, [class](../vs140/class--C#-Reference-.md), the keyword is replaced by the shortcut. For more information, see [Default Expansions in C#](../Topic/Visual%20C%23%20Code%20Snippets.md).  
  
## Selection in Completion Lists  
 **Committed by typing the following characters:**  
 Specifies all characters that execute IntelliSense automatic completion for the selected item in completion list, after they are typed.  
  
 **Committed by pressing the space bar**  
 Specifies to include the action of pressing the space bar to execute IntelliSense automatic completion for the selected item in completion list.  
  
 **Add new line on enter at end of fully typed word**  
 Specifies that if you type all the characters for an entry in the completion list and then press ENTER, a new line is created automatically and the cursor moves to the new line.  
  
 For example, if you type `else` and then press ENTER, the following appears in the editor:  
  
 `else`  
  
 `|` (cursor location)  
  
 However, if you type only `el` and then press ENTER, the following appears in the editor:  
  
 `else|` (cursor location)  
  
## IntelliSense Member Selection  
 **Pre-selects most recently used member**  
 When this option is selected, IntelliSense pre-selects the members that you have recently selected in the pop-up List Members box for automatic object name completion, during your current session in the integrated development environment (IDE). The history of most recently used members is cleared between each session in the IDE. For more information, see [IntelliSense for Most Recently Used Members](../vs140/IntelliSense-for-Most-Recently-Used-Members.md).  
  
## See Also  
 [General, Environment, Options Dialog Box](../vs140/General--Environment--Options-Dialog-Box.md)   
 [Documenting Your Code with XML](../vs140/XML-Documentation-Comments--C#-Programming-Guide-.md)   
 [Using IntelliSense](../vs140/Using-IntelliSense.md)