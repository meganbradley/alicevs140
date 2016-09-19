---
title: "-- Implementation Comment"
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
H1: // Implementation Comment
ms.assetid: 4d799c07-8e71-4a6b-90ab-8282d6ff48ce
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -- Implementation Comment
The `// Implementation` section is the most important part of any MFC class declaration.  
  
 This section houses all implementation details. Both member variables and member functions can appear in this section. Everything below this line could change in a future release of MFC. Unless you cannot avoid it, you should not rely on details below the `// Implementation` line. In addition, members declared below the implementation line are not documented, although some implementation is discussed in technical notes. Overrides of virtual functions in the base class reside in this section, regardless of which section the base class function is defined in, because the fact that a function overrides the base class implementation is considered an implementation detail. Typically, these members are protected, but not always.  
  
 Notice from the `CStdioFile` listing under [An Example of the Comments](../vs140/An-Example-of-the-Comments.md) that members declared below the `// Implementation` comment may be declared as **public**, `protected`, or `private`. You should only use these members with caution, because they may change in the future. Declaring a group of members as **public** may be necessary for the class library implementation to work correctly. However, this does not mean that you may safely use the members so declared.  
  
> [!NOTE]
>  You may find comments of the remaining types either above or below the `// Implementation` comment. In either case, they describe the kinds of members declared below them. If they occur below the `// Implementation` comment, you should assume that the members may change in future versions of MFC.  
  
## See Also  
 [Using the MFC Source Files](../vs140/Using-the-MFC-Source-Files.md)   
 [An Example of the Comments](../vs140/An-Example-of-the-Comments.md)   
 [// Constructors Comment](../vs140/---Constructors-Comment.md)   
 [// Attributes Comment](../vs140/---Attributes-Comment.md)   
 [// Operations Comment](../vs140/---Operations-Comment.md)   
 [// Overridables Comment](../vs140/---Overridables-Comment.md)