---
title: "Code Snippets"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 85976ad9-4c9a-4e7b-896e-66ec6f955199
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Code Snippets
Code snippets are small blocks of reusable code that can be inserted in a code file using a context menu command or a combination of hotkeys. They typically contain commonly-used code blocks such as try-finally or if-else blocks, but they can be used to insert entire classes or methods.  
  
## Expansion Snippets and Surround-With Snippets  
 In Visual Studio there are two kinds of code snippet: expansion snippets, which are added at a specified insertion point and may replace a snippet shortcut, and surround-with snippets (C# and C++ only), which are added around a selected block of code.  
  
 An example of an insertion snippet: in C# the shortcut tryf is used to insert a try-finally block:  
  
```  
try  
{  
  
}  
finally  
{  
  
}  
  
```  
  
 You can insert this snippet by clicking **Insert Snippet** in the context menu of the code window, then **Visual C#**, then type `tryf`, then TAB, or you can type `tryf` and press TAB + TAB.  
  
 An example of a surround-with snippet: in C++ the shortcut `if` can be used either as an insertion snippet or as a surround-with snippet. If you select a line of code (for example `return FALSE;`), and then click **Surround With**, then **if**, the snippet is expanded around the line:  
  
```  
if (true)  
{  
    return FALSE;  
}  
  
```  
  
## Snippet Replacement Parameters  
 Snippets can contain replacement parameters, which are placeholders that you must replace to fit the precise code you are writing. In the previous example `true` is a replacement parameter, which you would replace with the appropriate condition. The replacement you make is repeated for every instance of the same replacement parameter in the snippet.  
  
 For example, in Visual Basic there is a code snippet that inserts a property. Click **Insert Snippet** on the context menu of the code window, then **Code Patterns**, then **Properties, Procedures, Events**, then Define a property. The following code is inserted:  
  
```  
Private newPropertyValue As String  
Public Property NewProperty() As String  
    Get  
        Return newPropertyValue  
    End Get  
    Set(ByVal value As String)  
        newPropertyValue = value  
    End Set  
End Property  
  
```  
  
 If you change `newPropertyValue` to `m_property`, then every instance of `newPropertyValue` is changed. If you change `String` to `Int` in the property declaration, then the value in the set method is also changed to `Int`.  
  
## Code Snippet Manager  
 You can see all the code snippets that are currently installed, plus their location on disk, by clicking **Tools/Code Snippets Manager**. Snippets are displayed by language.  
  
 You can add and remove snippet directories with the **Add** and **Remove** buttons in the **Code Snippets Manager** dialog. To add individual code snippets, use the **Import** button.  
  
## See Also  
 [Walkthrough: Creating a Code Snippet](../vs140/Walkthrough--Creating-a-Code-Snippet.md)   
 [How to: Distribute Code Snippets](../vs140/How-to--Distribute-Code-Snippets.md)   
 [Best Practices for Using Code Snippets](../vs140/Best-Practices-for-Using-Code-Snippets.md)   
 [Troubleshooting Snippets](../vs140/Troubleshooting-Snippets.md)   
 [Visual C# Code Snippets](../Topic/Visual%20C%23%20Code%20Snippets.md)   
 [Visual C++ Code Snippets](../vs140/Visual-C---Code-Snippets.md)   
 [Code Snippets Schema Reference](../vs140/Code-Snippets-Schema-Reference.md)