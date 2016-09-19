---
title: "CDaoException::m_pErrorInfo"
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
ms.assetid: b1dfb865-245a-4b2c-895d-f6341c05b371
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoException::m_pErrorInfo
Contains a pointer to a `CDaoErrorInfo` structure that provides information on the DAO error object that you last retrieved by calling [GetErrorInfo](../vs140/CDaoException--GetErrorInfo.md).  
  
## Remarks  
 This object contains the following information:  
  
|CDaoErrorInfo member|Information|Meaning|  
|--------------------------|-----------------|-------------|  
|**m_lErrorCode**|Error Code|The DAO error code|  
|`m_strSource`|Source|The name of the object or application that originally generated the error|  
|`m_strDescription`|Description|A descriptive string associated with the error|  
|`m_strHelpFile`|Help File|A path to a Windows Help file in which the user can get information about the problem|  
|**m_lHelpContext**|Help Context|The context ID for a topic in the DAO Help file|  
  
 For full details about the information contained in the `CDaoErrorInfo` object, see the [CDaoErrorInfo](../vs140/CDaoErrorInfo-Structure.md) structure.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoException Class](../vs140/CDaoException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoException::m_scode](../vs140/CDaoException--m_scode.md)   
 [CDaoException::m_nAfxDaoError](../vs140/CDaoException--m_nAfxDaoError.md)