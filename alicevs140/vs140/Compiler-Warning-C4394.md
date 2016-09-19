---
title: "Compiler Warning C4394"
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
ms.topic: error-reference
ms.assetid: 5de94de0-17e3-4e7c-92f4-5c3c1b825120
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4394
'function' : per-appdomain symbol should not be marked with __declspec(dllexport)  
  
 A function marked with the [appdomain](../vs140/appdomain.md)`__declspec` modifier is compiled to MSIL (not to native), and export tables ([export](../vs140/export.md)`__declspec` modifier) are not supported for managed functions.  
  
 You can declare a managed function to have public accessibility. For more information, see [Type Visibility](../Topic/How%20to:%20Define%20and%20Consume%20Classes%20and%20Structs%20\(C++-CLI\).md#BKMK_Type_visibility) and [Member visibility](../Topic/How%20to:%20Define%20and%20Consume%20Classes%20and%20Structs%20\(C++-CLI\).md#BKMK_Member_visibility).  
  
 C4394 is always issued as an error.  You can turn off this warning with the `#pragma warning` or **/wd**; see [warning](../vs140/warning.md) or [/w, /Wn, /WX, /Wall, /wln, /wdn, /wen, /won (Warning Level)](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md) for more information.  
  
## Example  
 The following sample generates C4394.  
  
```  
// C4394.cpp  
// compile with: /clr /c  
__declspec(dllexport) __declspec(appdomain) int g1 = 0;   // C4394  
__declspec(dllexport) int g2 = 0;   // OK  
```