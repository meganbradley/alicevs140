---
title: "Compiler Error C3632"
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
ms.assetid: a04e3217-f5a1-4461-a1db-d69fd096d468
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3632
'event': illegal style of event for construct  
  
 [__event](../vs140/__event.md) declarations are not valid in all constructs.  
  
 C3632 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3632:  
  
```  
// C3632.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
public __gc __interface I  
{  
   __event void sna();   // C3632  
};  
  
// use the following as an example  
__delegate void MyDel();  
public __gc __interface I2  
{  
   __event MyDel* sna;  
};  
  
int main()  
{  
}  
```