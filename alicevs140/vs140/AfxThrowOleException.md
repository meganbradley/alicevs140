---
title: "AfxThrowOleException"
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
ms.topic: article
ms.assetid: 90af5c1b-e875-4194-bab7-c04da1d0ef32
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowOleException
Creates an object of type `COleException` and throws an exception.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxThrowOleException(  
   SCODE sc   
);  
void AFXAPI AfxThrowOleException(  
   HRESULT hr   
);  
```  
  
#### Parameters  
 `sc`  
 An OLE status code that indicates the reason for the exception.  
  
 `hr`  
 Handle to a result code that indicates the reason for the exception.  
  
## Remarks  
 The version that takes an `HRESULT` as an argument converts that result code into the corresponding `SCODE`. For more information on `HRESULT` and `SCODE`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** <afxdisp.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleException Class](../vs140/COleException-Class.md)   
 [THROW](../vs140/THROW--MFC-.md)