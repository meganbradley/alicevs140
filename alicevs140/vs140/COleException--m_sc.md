---
title: "COleException::m_sc"
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
ms.assetid: cdefe0c2-0139-4b9e-975a-530e8261c2be
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleException::m_sc
This data member holds the OLE status code that indicates the reason for the exception.  
  
## Syntax  
  
```  
  
SCODE m_sc;  
```  
  
## Remarks  
 This variable's value is set by [AfxThrowOleException](../vs140/AfxThrowOleException.md).  
  
 For more information on `SCODE`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCOleContainer#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#22)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleException Class](../vs140/COleException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AfxThrowOleException](../vs140/AfxThrowOleException.md)