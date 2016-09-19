---
title: "Specifiers"
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
ms.topic: language-reference
ms.assetid: 8b14e844-9880-4571-8779-28c8efe44633
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifiers
This topic describes the *decl-specifiers* (declaration specifiers) component of a [declaration](../vs140/Declarations.md).  
  
 The following placeholders and language keywords are declaration specifiers:  
  
 *storage-class-specifier*  
  
 *type-specifier*  
  
 *function-specifier*  
  
 [friend](../vs140/friend--C---.md)  
  
 [typedef](assetId:///cc96cf26-ba93-4179-951e-695d1f5fdcf1)  
  
 [__declspec](../vs140/__declspec.md) `(` *extended-decl-modifier-seq* `)`  
  
## Remarks  
 The *decl-specifiers* part of a declaration is the longest sequence of *decl-specifiers* that can be taken to mean a type name, not including the pointer or reference modifiers. The remainder of the declaration is the *declarator*, which includes the name introduced.  
  
 The following table lists four declarations, and then lists each declaration's *decl-specifers* and *declarator* component separately.  
  
|Declaration|*decl-specifiers*|`declarator`|  
|-----------------|------------------------|------------------|  
|`char *lpszAppName;`|`char`|`*lpszAppName`|  
|`typedef char * LPSTR;`|`char`|`*LPSTR`|  
|`const int func1();`|`const int`|`func1`|  
|`volatile void *pvvObj;`|`volatile void`|`*pvvObj`|  
  
 Because `signed`, `unsigned`, `long`, and `short` all imply `int`, a `typedef` name following one of these keywords is taken to be a member of *declarator-list,* not of *decl-specifiers*.  
  
> [!NOTE]
>  Because a name can be redeclared, its interpretation is subject to the most recent declaration in the current scope. Redeclaration can affect how names are interpreted by the compiler, especially `typedef` names.  
  
## See Also  
 [Declarations](../vs140/Declarations.md)