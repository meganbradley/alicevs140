---
title: "CSimpleException::CSimpleException"
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
ms.topic: reference
ms.assetid: 5b58a1dd-db72-4d09-8760-da4fad342539
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleException::CSimpleException
The constructor.  
  
## Syntax  
  
```  
  
      CSimpleException( );   
explicit CSimpleException(  
   BOOL bAutoDelete  
);  
```  
  
#### Parameters  
 `bAutoDelete`  
 Specify **TRUE** if the memory for the `CSimpleException` object has been allocated on the heap. This will cause the `CSimpleException` object to be deleted when the **Delete** member function is called to delete the exception. Specify **FALSE** if the `CSimpleException` object is on the stack or is a global object. In this case, the `CSimpleException` object will not be deleted when the **Delete** member function is called.  
  
## Remarks  
 You would normally never need to call this constructor directly. A function that throws an exception should create an instance of a `CException`-derived class and call its constructor, or it should use one of the MFC throw functions, such as [AfxThrowFileException](../vs140/AfxThrowFileException.md), to throw a predefined type.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CSimpleException Class](../vs140/CSimpleException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)