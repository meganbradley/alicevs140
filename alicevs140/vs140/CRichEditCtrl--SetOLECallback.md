---
title: "CRichEditCtrl::SetOLECallback"
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
ms.assetid: 56e9c467-2d12-4dc3-84a7-15827c735ea4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::SetOLECallback
Gives this `CRichEditCtrl` object an **IRichEditOleCallback** object to use to access OLE-related resources and information.  
  
## Syntax  
  
```  
  
      BOOL SetOLECallback(  
   IRichEditOleCallback* pCallback   
);  
```  
  
#### Parameters  
 `pCallback`  
 Pointer to an [IRichEditOleCallback](http://msdn.microsoft.com/library/windows/desktop/bb774308) object that this `CRichEditCtrl` object will use to get OLE-related resources and information.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 This `CRichEditCtrl` object will call [IUnknown::AddRef](http://msdn.microsoft.com/library/windows/desktop/ms691379) to increment the usage count for the COM object specified by `pCallback`.  
  
 For more information, see [EM_SETOLECALLBACK](http://msdn.microsoft.com/library/windows/desktop/bb774252) message and [IRichEditOleCallback](http://msdn.microsoft.com/library/windows/desktop/bb774308) interface in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetIRichEditOle](../vs140/CRichEditCtrl--GetIRichEditOle.md)