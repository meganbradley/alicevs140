---
title: "Compiler Error C3856"
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
ms.assetid: 242d9322-c325-4f20-be58-b2be6da56d60
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3856
'type': class is not a class type  
  
 The most common cause for this error is when there are more generic or template parameter lists at the point of definition than there were at the point of declaration.  
  
 The following sample generates C3856:  
  
```  
// C3856.cpp  
template <class T>   
struct S {  
   template <class T1>   
   struct S1;   
   void f();   
};  
  
template <class T>   // C3856  
template <class T1>  
template <class T2>  // extra template parameter list in definition  
struct S<T>::S1{};  
```  
  
 Possible resolution:  
  
```  
// C3856b.cpp  
// compile with: /c  
template <class T>   
struct S {  
   template <class T1>   
   struct S1;   
   void f();   
};  
  
template <class T>  
template <class T1>  
struct S<T>::S1{};  
```  
  
 C3856 can also occur when using generics:  
  
```  
// C3856c.cpp  
// compile with: /clr  
generic <class T>  
ref struct GS {  
   generic <class U>  
   ref struct GS2;  
};  
  
generic <class T>  
generic <class U>  
generic <class V>  
ref struct GS<T>::GS2 {};   // C3856  
```  
  
 Possible resolution:  
  
```  
// C3856d.cpp  
// compile with: /clr /c  
generic <class T>  
ref struct GS {  
   generic <class U>  
   ref struct GS2;  
};  
  
generic <class T>  
generic <class U>  
ref struct GS<T>::GS2 {};  
```