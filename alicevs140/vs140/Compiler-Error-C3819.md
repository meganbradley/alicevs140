---
title: "Compiler Error C3819"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: fc279aa6-bcc1-4f99-88e5-cf9a2a1913dd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3819
wrong number of parameters in 'property'  
  
 An accessor function for a [__property](../vs140/__property.md) had the wrong number of parameters.  
  
 C3819 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3819:  
  
```  
// C3819.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__gc struct AtClass {  
   __property int get_bad() {  
      return _i;  
   }  
  
   __property void set_bad() {   // C3819  
   }  
  
   // uncomment this access definition to resolve  
   /*  
   __property void set_bad(int i) {  
      _i = i;  
   }  
   */  
public:  
   int _i;  
};  
  
int main() {  
}  
```