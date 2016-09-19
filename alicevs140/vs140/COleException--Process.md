---
title: "COleException::Process"
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
ms.assetid: ada95e01-2f9c-4169-9cc2-c5c1b9e769b3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleException::Process
Call the **Process** member function to translate a caught exception into an OLE status code.  
  
## Syntax  
  
```  
  
      static SCODE PASCAL Process(  
   const CException* pAnyException   
);  
```  
  
#### Parameters  
 *pAnyException*  
 Pointer to a caught exception.  
  
## Return Value  
 An OLE status code.  
  
## Remarks  
  
> [!NOTE]
>  This function is **static**.  
  
 For more information on `SCODE`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [COleDispatchDriver::CreateDispatch](../vs140/COleDispatchDriver--CreateDispatch.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleException Class](../vs140/COleException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException Class](../vs140/CException-Class.md)