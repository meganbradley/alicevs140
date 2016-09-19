---
title: "How to: Create XML Documentation in Visual Basic"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 27b5b06c-09b9-496a-8245-f9542d846230
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create XML Documentation in Visual Basic
This example shows how to add XML documentation comments to your code.  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
### To create XML documentation for a type or member  
  
1.  In the **Code Editor**, position your cursor on the line above the type or member for which you want to create documentation.  
  
2.  Type `'''` (three single-quotation marks).  
  
     An XML skeleton for the type or member is added in the **Code Editor**.  
  
3.  Add descriptive information between the appropriate tags.  
  
    > [!NOTE]
    >  If you add additional lines within the XML documentation block, each line must begin with `'''`.  
  
4.  Add additional code that uses the type or member with the new XML documentation comments.  
  
     IntelliSense displays the text from the <summary\> tag for the type or member.  
  
5.  Compile the code to generate an XML file containing the documentation comments. For more information, see [/doc](../vs140/-doc.md).  
  
## See Also  
 [Documenting Your Code with XML (Visual Basic)](../vs140/Documenting-Your-Code-with-XML--Visual-Basic-.md)   
 [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)   
 [/doc](../vs140/-doc.md)