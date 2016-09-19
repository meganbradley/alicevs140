---
title: "Compiler Error C3223"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1f4380b4-0413-40db-a868-62f97babaf78
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3223
'property' : you cannot apply 'typeid' to a property  
  
 You cannot apply [typeid](../Topic/typeid%20%20\(C++%20Component%20Extensions\).md) to a property.  
  
## Example  
 The following sample generates C3223.  
  
```  
// C3223.cpp  
// compile with: /clr  
ref class R {  
public:  
   property int myprop;  
};  
  
int main() {  
   System::Type^ type2 = R::myprop::typeid;   // C3223  
}  
```