---
title: "Data type(s) of the type parameter(s) cannot be inferred from these arguments because more than one type is possible"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 79287e1f-7070-4a71-96d2-aee0a0c9d8bd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data type(s) of the type parameter(s) cannot be inferred from these arguments because more than one type is possible
Data type(s) of the type parameter(s) cannot be inferred from these arguments because more than one type is possible. Specifying the data type(s) explicitly might correct this error.  
  
 This error occurs when overload resolution has failed. It occurs as a subordinate message that indicates why a particular overload candidate has been eliminated. The error explains that if type inference is applied to determine the data type of the type parameters of the called generic procedure, the compiler finds more than one possible data type for at least one of them.  
  
> [!NOTE]
>  When specifying arguments is not an option (for example, for query operators in query expressions), the error message appears without the second sentence.  
  
 For more information and examples, see [Data type(s) of the type parameter(s) in method '<methodname\>' cannot be inferred from these arguments because more than one type is possible](../vs140/Data-type-s--of-the-type-parameter-s--in-method---methodname---cannot-be-inferred-from-these-arguments-because-more-than-one-type-is-possible.md).  
  
 **Error ID:** BC36653 and BC36650  
  
## See Also  
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)