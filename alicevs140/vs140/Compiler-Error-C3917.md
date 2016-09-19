---
title: "Compiler Error C3917"
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
ms.assetid: a24cd0c9-262f-46e5-9488-1c01f945933d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3917
'property': obsolete construct declaration style  
  
 A property or event definition used syntax from a previous version.  
  
 If you want to use syntax from a previous version, use [/clr:oldSyntax](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
 For more information, see [property](../vs140/property---C---Component-Extensions-.md).  
  
## Example  
  
```  
// C3917.cpp  
// compile with: /clr /c  
public ref class  C {  
private:  
   int m_length;  
public:  
   C() {  
      m_length = 0;  
   }  
  
   property int get_Length();   // C3917  
  
   // The correct property definition:  
   property int Length {  
      int get() {  
         return m_length;  
      }  
  
      void set( int i ) {  
         m_length = i;  
      }  
   }  
};  
```