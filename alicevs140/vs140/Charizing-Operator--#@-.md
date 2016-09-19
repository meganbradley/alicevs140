---
title: "Charizing Operator (#@)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dee03314-d27c-4063-965c-64756efbef22
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Charizing Operator (#@)
**Microsoft Specific**  
  
 The charizing operator can be used only with arguments of macros. If **#@** precedes a formal parameter in the definition of the macro, the actual argument is enclosed in single quotation marks and treated as a character when the macro is expanded. For example:  
  
```  
#define makechar(x)  #@x  
```  
  
 causes the statement  
  
```  
a = makechar(b);  
```  
  
 to be expanded to  
  
```  
a = 'b';  
```  
  
 The single-quotation character cannot be used with the charizing operator.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Preprocessor Operators](../vs140/Preprocessor-Operators.md)