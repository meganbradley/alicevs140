---
title: "-- Attributes Comment"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: // Attributes Comment
ms.assetid: 96388e11-42df-4994-aedf-decd152961a7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -- Attributes Comment
The `// Attributes` section of an MFC class declaration contains the public attributes (or properties) of the object. Typically these are member variables, or Get/Set functions. The "Get" and "Set" functions may or may not be virtual. The "Get" functions are usually **const**, because in most cases they do not have side effects. These members are normally public; protected and private attributes are typically found in the implementation section.  
  
 In the sample listing from class `CStdioFile`, under [An Example of the Comments](../vs140/An-Example-of-the-Comments.md), the list includes one member variable, `m_pStream`. Class `CDC` lists nearly 20 members under this comment.  
  
> [!NOTE]
>  Large classes, such as `CDC` and `CWnd`, may have so many members that simply listing all the attributes in one group would not add much to clarity. In such cases, the class library uses other comments as headings to further delineate the members. For example, `CDC` uses `// Device-Context Functions`, `// Drawing Tool Functions`, `// Drawing Attribute Functions`, and more. Groups that represent attributes will follow the usual syntax described above. Many OLE classes have an implementation section called `// Interface Maps`.  
  
## See Also  
 [Using the MFC Source Files](../vs140/Using-the-MFC-Source-Files.md)   
 [An Example of the Comments](../vs140/An-Example-of-the-Comments.md)   
 [// Implementation Comment](../vs140/---Implementation-Comment.md)   
 [// Constructors Comment](../vs140/---Constructors-Comment.md)   
 [// Operations Comment](../vs140/---Operations-Comment.md)   
 [// Overridables Comment](../vs140/---Overridables-Comment.md)