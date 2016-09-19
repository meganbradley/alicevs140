---
title: "Compiler Error C2626"
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
ms.assetid: 4c283ad0-251b-4571-bc18-468b9836746f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2626
'identifier': a private or protected data member is not allowed in an anonymous struct or union  
  
 A member of an anonymous struct or union must have public access.  
  
 The following sample generates C2626:  
  
```  
// C2626.cpp  
int main() {  
   union {  
   protected:  
      int j;     // C2626, j is protected  
   private:  
      int k;     // C2626, k is private  
   };  
}  
```  
  
 To fix this issue, remove any private or protected tags:  
  
```  
// C2626b.cpp  
int main() {  
   union {  
   public:  
      int i;   // OK, i is public  
   };  
}  
```