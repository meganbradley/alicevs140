---
title: "CDaoException::m_scode"
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
ms.assetid: f03ec453-b3fa-45d2-8680-664bd92a4303
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoException::m_scode
Contains a value of type `SCODE` that describes the error.  
  
## Remarks  
 This is an OLE code. You will seldom need to use this value because, in almost all cases, more specific MFC or DAO error information is available in the other `CDaoException` data members.  
  
 For information about `SCODE`, see the topic [Structure of OLE Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The `SCODE` data type maps to the `HRESULT` data type.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoException Class](../vs140/CDaoException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoException::m_pErrorInfo](../vs140/CDaoException--m_pErrorInfo.md)   
 [CDaoException::m_nAfxDaoError](../vs140/CDaoException--m_nAfxDaoError.md)