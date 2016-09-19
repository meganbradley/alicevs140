---
title: "Compiler Warning (level 4) C4634"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e3496ce-2ac7-43d0-a48a-f514c950e81d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4634
XML document comment: cannot be applied:  reason  
  
 XML documentation tags can not be applied to all C++ constructs.  For example, you cannot add a documentation comment to a namespace or template.  
  
 For more information, see [XML Documentation](../vs140/XML-Documentation--Visual-C---.md).  
  
## Example  
 The following sample generates C4634.  
  
```  
// C4634.cpp  
// compile with: /W4 /doc /c  
/// This is a namespace.   // C4634  
namespace hello {  
   class MyClass  {};  
};  
```  
  
## Example  
 The following sample generates C4634.  
  
```  
// C4634_b.cpp  
// compile with: /W4 /doc /c  
/// This is a template.   // C4634  
template <class T>  
class MyClass  {};  
```