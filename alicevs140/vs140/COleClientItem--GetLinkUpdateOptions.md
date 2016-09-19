---
title: "COleClientItem::GetLinkUpdateOptions"
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
ms.assetid: 66087ed6-4ded-49e5-a583-afbd23aa2a9f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetLinkUpdateOptions
Call this function to get the current value of the link-update option for the OLE item.  
  
## Syntax  
  
```  
  
OLEUPDATE GetLinkUpdateOptions( );  
```  
  
## Return Value  
 One of the following values:  
  
-   `OLEUPDATE_ALWAYS` Update the linked item whenever possible. This option supports the Automatic link-update radio button in the Links dialog box.  
  
-   `OLEUPDATE_ONCALL` Update the linked item only on request from the container application (when the [UpdateLink](../vs140/COleClientItem--UpdateLink.md) member function is called). This option supports the Manual link-update radio button in the Links dialog box.  
  
## Remarks  
 This is an advanced operation.  
  
 This function is called automatically by the [COleLinksDialog](../vs140/COleLinksDialog-Class.md) class.  
  
 For more information, see [IOleLink::GetUpdateOptions](http://msdn.microsoft.com/library/windows/desktop/ms680100) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::SetLinkUpdateOptions](../vs140/COleClientItem--SetLinkUpdateOptions.md)   
 [COleLinksDialog Class](../vs140/COleLinksDialog-Class.md)