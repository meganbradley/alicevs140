---
title: "Compiler Error C2599"
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
ms.assetid: 88515f36-7589-47e2-862e-0de8b18d6668
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2599
'enum' : forward declaration of enum type is not allowed  
  
 The compiler no longer supports forward declaration of a managed enumeration.  
  
 Forward declaration of an enum type is not allowed under [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md).  
  
 The following sample generates C2599:  
  
```  
// C2599.cpp  
// compile with: /clr /c  
enum class Status;   // C2599  
  
enum class Status2 { stop2, hold2, go2};   
  
ref struct MyStruct {  
   // Delete the following line to resolve.  
   Status m_status;  
  
   Status2 m_status2;   // OK  
};  
  
enum class Status { stop, hold, go };  
```