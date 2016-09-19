---
title: "Compiler Warning (level 1) C4662"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7efda273-d04a-47b7-ad65-ff1ff94b5ffc
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4662
explicit instantiation; template-class 'identifier1' has no definition from which to specialize 'identifier2'  
  
 The specified template-class was declared, but not defined.  
  
## Example  
  
```  
// C4662.cpp  
// compile with: /W1 /LD  
template<class T, int i> class MyClass; // no definition  
template MyClass< int, 1>;              // C4662  
```