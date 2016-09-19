---
title: "COleException Class"
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
ms.assetid: 2571e9fe-26cc-42f0-9ad9-8ad5b4311ec1
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleException Class
Represents an exception condition related to an OLE operation.  
  
## Syntax  
  
```  
class COleException : public CException  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[COleException::Process](#coleexception__process)|Translates a caught exception into an OLE return code.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[COleException::m_sc](#coleexception__m_sc)|Contains the status code that indicates the reason for the exception.|  
  
## Remarks  
 The `COleException` class includes a public data member that holds the status code indicating the reason for the exception.  
  
 In general, you should not create a `COleException` object directly; instead, you should call [AfxThrowOleException](../vs140/AfxThrowOleException.md).  
  
 For more information on exceptions, see the articles [Exception Handling (MFC)](../vs140/Exception-Handling-in-MFC.md) and [Exceptions: OLE Exceptions](../vs140/Exceptions--OLE-Exceptions.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CException](../vs140/CException-Class.md)  
  
 `COleException`  
  
## Requirements  
 **Header:** afxdisp.h  
  
##  <a name="coleexception__m_sc"></a>  COleException::m_sc  
 This data member holds the OLE status code that indicates the reason for the exception.  
  
```  
SCODE m_sc;  
  
```  
  
### Remarks  
 This variable's value is set by [AfxThrowOleException](../vs140/AfxThrowOleException.md).  
  
 For more information on `SCODE`, see                         [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Example  
 [!CODE [NVC_MFCOleContainer#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#22)]  
  
##  <a name="coleexception__process"></a>  COleException::Process  
 Call the **Process** member function to translate a caught exception into an OLE status code.  
  
```  
static SCODE PASCAL Process(    const CException* pAnyException );  
  
```  
  
### Parameters  
 *pAnyException*  
 Pointer to a caught exception.  
  
### Return Value  
 An OLE status code.  
  
### Remarks  
  
> [!NOTE]
>  This function is **static**.  
  
 For more information on `SCODE`, see                         [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Example  
  See the example for [COleDispatchDriver::CreateDispatch](../vs140/COleDispatchDriver-Class.md#coledispatchdriver__createdispatch).  
  
## See Also  
 [MFC Sample CALCDRIV](../vs140/Visual-C---Samples.md)   
 [Base Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)