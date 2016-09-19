---
title: "CSimpleException Class"
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
ms.assetid: be0eb8ef-e5b9-47d6-b0fb-efaff2d1e666
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleException Class
This class is a base class for resource-critical MFC exceptions.  
  
## Syntax  
  
```  
class AFX_NOVTABLE CSimpleException : public CException  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleException::CSimpleException](#csimpleexception__csimpleexception)|The constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSimpleException::GetErrorMessage](#csimpleexception__geterrormessage)|Provides text about an error that has occurred.|  
  
## Remarks  
 `CSimpleException` is the base class for resource-critical MFC exceptions and handles the ownership and initialization of an error message. The following classes use `CSimpleException` as their base class:  
  
|||  
|-|-|  
|[CMemoryException Class](../vs140/CMemoryException-Class.md)|Out-of-memory exception|  
|[CNotSupportedException Class](../vs140/CNotSupportedException-Class.md)|Requests for an unsupported operation|  
|[CResourceException Class](../vs140/CResourceException-Class.md)|Windows resource not found or not creatable|  
|[CUserException Class](../vs140/CUserException-Class.md)|Exception that indicates a resource could not be found|  
|[CInvalidArgException Class](../vs140/CInvalidArgException-Class.md)|Exception that indicates an invalid argument|  
  
 Because `CSimpleException` is an abstract base class, you cannot declare a `CSimpleException` object directly. Instead, you must declare derived objects such as those in the previous table. If you are declaring your own derived class, use the previous classes as a model.  
  
 For more information, see the [CException Class](../vs140/CException-Class.md) topic and [Exception Handling (MFC)](../vs140/Exception-Handling-in-MFC.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CException](../vs140/CException-Class.md)  
  
 `CSimpleException`  
  
## Requirements  
 **Header:** afx.h  
  
##  <a name="csimpleexception__csimpleexception"></a>  CSimpleException::CSimpleException  
 The constructor.  
  
```  
CSimpleException( ); explicit CSimpleException(    BOOL  bAutoDelete );  
  
```  
  
### Parameters  
 `bAutoDelete`  
 Specify **TRUE** if the memory for the `CSimpleException` object has been allocated on the heap. This will cause the `CSimpleException` object to be deleted when the **Delete** member function is called to delete the exception. Specify **FALSE** if the `CSimpleException` object is on the stack or is a global object. In this case, the `CSimpleException` object will not be deleted when the **Delete** member function is called.  
  
### Remarks  
 You would normally never need to call this constructor directly. A function that throws an exception should create an instance of a `CException`-derived class and call its constructor, or it should use one of the MFC throw functions, such as [AfxThrowFileException](../vs140/AfxThrowFileException.md), to throw a predefined type.  
  
##  <a name="csimpleexception__geterrormessage"></a>  CSimpleException::GetErrorMessage  
 Call this member function to provide text about an error that has occurred.  
  
```  
virtual BOOL GetErrorMessage(    LPTSTR  lpszError, UINT  nMaxError, PUNIT  pnHelpContext =  NULL );  
  
```  
  
### Parameters  
 `lpszError`  
 A pointer to a buffer that will receive an error message.  
  
 `nMaxError`  
 The maximum number of characters the buffer can hold, including the **NULL** terminator.  
  
 `pnHelpContext`  
 The address of a **UINT** that will receive the help context ID. If **NULL**, no ID will be returned.  
  
### Return Value  
 Nonzero if the function is successful; otherwise 0 if no error message text is available.  
  
### Remarks  
 For more information, see [CException::GetErrorMessage](../vs140/CFileException-Class.md#cfileexception__geterrormessage).  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException Class](../vs140/CException-Class.md)   
 [Exception Handling (MFC)](../vs140/Exception-Handling-in-MFC.md)