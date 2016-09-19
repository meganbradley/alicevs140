---
title: "Compiler Error C3888"
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
ms.assetid: 40820812-79c5-4dcd-a19d-b4164d25fc8a
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3888
'name' : the const expression associated with this literal data member is not supported by C++/CLI  
  
 The *name* data member that is declared with the [literal](../vs140/literal--C---Component-Extensions-.md) keyword is initialized with a value the compiler does not support. The compiler supports only constant integral, enum, or string types. The likely cause for the **C3888** error is that the data member is initialized with a byte array.  
  
### To correct this error  
  
1.  Check that the declared literal data member is a supported type.  
  
## See Also  
 [literal (Visual C++)](../vs140/literal--C---Component-Extensions-.md)