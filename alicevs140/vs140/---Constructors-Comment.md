---
title: "-- Constructors Comment"
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
H1: // Constructors Comment
ms.assetid: f400774e-ba85-49ed-85b7-70ef2f7dcb2b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -- Constructors Comment
The `// Constructors` section of an MFC class declaration declares constructors (in the C++ sense) as well as any initialization functions required to really use the object. For example, `CWnd::Create` is in the constructors section because before you use the `CWnd` object, it must be "fully constructed" by first calling the C++ constructor and then calling the **Create** function. Typically, these members are public.  
  
 For example, class `CStdioFile` has three constructors, one of which is shown in the listing under [An Example of the Comments](../vs140/An-Example-of-the-Comments.md).  
  
## See Also  
 [Using the MFC Source Files](../vs140/Using-the-MFC-Source-Files.md)   
 [// Implementation Comment](../vs140/---Implementation-Comment.md)   
 [// Attributes Comment](../vs140/---Attributes-Comment.md)   
 [// Operations Comment](../vs140/---Operations-Comment.md)   
 [// Overridables Comment](../vs140/---Overridables-Comment.md)