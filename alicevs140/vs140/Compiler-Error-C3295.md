---
title: "Compiler Error C3295"
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
ms.assetid: 83f0aa4d-0e0a-4905-9f66-fcf9991fc07a
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3295
'#pragma pragma' can only be used at global or namespace scope  
  
 Some pragmas cannot be used in a function.  See [Pragma Directives](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md) for more information.  
  
## Example  
 The following sample generates C3295.  
  
```  
// C3295.cpp  
int main() {  
   #pragma managed   // C3295  
}  
```