---
title: "Compiler Warning (level 1) C4526"
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
ms.assetid: 490f8916-5fdc-4cad-b412-76c3382a5976
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4526
'function' : static member function cannot override virtual function 'virtual function'override ignored, virtual function will be hidden  
  
 The static member function meets the criteria to override the virtual function, which makes the member function both virtual and static.  
  
 The following code generates C4526:  
  
```  
// C4526.cpp  
// compile with: /W1 /c  
// C4526 expected  
struct myStruct1 {  
   virtual void __stdcall func( int ) = 0;  
};  
  
struct myStruct2: public myStruct1 {  
   static void __stdcall func( int );  
};  
```  
  
 The following are possible fixes:  
  
-   If the function was intended to override the base class virtual function, remove the static specifier.  
  
-   If the function was intended to be a static member function, rename it so it doesn't conflict with the base class virtual function.