---
title: "Compiler Error C3831"
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
ms.assetid: a125d8dc-b75a-4ea0-b6c7-fe7b119dba25
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3831
'member': 'class' cannot have a pinned data member or a member function returning a pinning pointer  
  
 [pin_ptr](../vs140/pin_ptr--C---CLI-.md) or [__pin](../vs140/__pin.md) was used incorrectly.  
  
 The following sample generates C3831:  
  
```  
// C3831a.cpp  
// compile with: /clr  
ref class Y  
{  
public:  
   int i;  
};  
  
ref class X  
{  
   pin_ptr<int> mbr_Y;   // C3831  
   int^ mbr_Y2;   // OK  
};  
  
int main() {  
   Y y;  
   pin_ptr<int> p = &y.i;  
}  
```  
  
 The following sample generates C3831:  
  
```  
// C3831b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__gc class Y  
{  
};  
  
__gc class X  
{  
   Y __pin * mbr_Y;   // C3831  
   Y * mbr_Y2;   // OK  
  
   Y __pin * mf_Y()  // C3831  
   {  
      Y __pin * pY = new Y();  
      return pY;  
   }  
  
   Y * mf_Y2()   // OK  
   {  
      Y * pY = new Y();  
      return pY;  
   }  
};  
```