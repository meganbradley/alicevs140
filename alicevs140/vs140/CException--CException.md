---
title: "CException::CException"
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
ms.assetid: a71d3efa-6483-4201-8ba5-99732c3f23ee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CException::CException
This member function constructs a `CException` object.  
  
## Syntax  
  
```  
  
      explicit CException(  
   BOOL bAutoDelete   
);  
```  
  
#### Parameters  
 *b_AutoDelete*  
 Specify **TRUE** if the memory for the `CException` object has been allocated on the heap. This will cause the `CException` object to be deleted when the **Delete** member function is called to delete the exception. Specify **FALSE** if the `CException` object is on the stack or is a global object. In this case, the `CException` object will not be deleted when the **Delete** member function is called.  
  
## Remarks  
 You would normally never need to call this constructor directly. A function that throws an exception should create an instance of a `CException`-derived class and call its constructor, or it should use one of the MFC throw functions, such as [AfxThrowFileException](../vs140/AfxThrowFileException.md), to throw a predefined type. This documentation is provided only for completeness.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CException Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)