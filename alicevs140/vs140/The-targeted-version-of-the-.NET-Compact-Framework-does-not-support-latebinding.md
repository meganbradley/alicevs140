---
title: "The targeted version of the .NET Compact Framework does not support latebinding"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b433014d-8422-46e8-ad55-321146a48186
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The targeted version of the .NET Compact Framework does not support latebinding
The version of the .NET Compact Framework you are working with does not support late binding.  
  
 **Error ID:** BC30762  
  
### To correct this error  
  
1.  Avoid calling functions, subs or properties on a variable declared as object.  
  
2.  Avoid using the object variable as an array.  
  
3.  Avoid using dictionary member access expressions with object variables.  
  
## See Also  
 [NotInBuild:Objects in Visual Basic](assetId:///85bd757a-a19e-45e1-af89-d68765f5ee3c)   
 [Special Characters in Code](../vs140/Special-Characters-in-Code--Visual-Basic-.md)