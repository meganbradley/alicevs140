---
title: "Compiler Error C3803"
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
ms.assetid: bad5fb9a-ed9a-4c15-96e7-cf06e200a50d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3803
'property': property has a type that is incompatible with one of its accessors 'accessor'  
  
 The type of a property defined with [property](../vs140/property--C---.md) does not match the return type for one of its accessor functions.  
  
 The following sample generates C3803:  
  
```  
// C3803.cpp  
struct A  
{  
   __declspec(property(get=GetIt)) int i;  
   char GetIt()  
   {  
      return 0;  
   }  
  
   /*  
   // try the following definition instead  
   int GetIt()  
   {  
      return 0;  
   }  
   */  
}; // C3803  
  
int main()  
{  
}  
```