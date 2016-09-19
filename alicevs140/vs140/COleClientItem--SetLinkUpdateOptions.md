---
title: "COleClientItem::SetLinkUpdateOptions"
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
ms.assetid: c2512d62-8a37-4579-95d6-027b57552e72
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::SetLinkUpdateOptions
Call this function to set the link-update option for the presentation of the specified linked item.  
  
## Syntax  
  
```  
  
      void SetLinkUpdateOptions(  
   OLEUPDATE dwUpdateOpt   
);  
```  
  
#### Parameters  
 *dwUpdateOpt*  
 The value of the link-update option for this item. This value must be one of the following:  
  
-   `OLEUPDATE_ALWAYS` Update the linked item whenever possible. This option supports the Automatic link-update radio button in the Links dialog box.  
  
-   `OLEUPDATE_ONCALL` Update the linked item only on request from the container application (when the [UpdateLink](../vs140/COleClientItem--UpdateLink.md) member function is called). This option supports the Manual link-update radio button in the Links dialog box.  
  
## Remarks  
 Typically, you should not change the update options chosen by the user in the Links dialog box.  
  
 For more information, see [IOleLink::SetUpdateOptions](http://msdn.microsoft.com/library/windows/desktop/ms680120) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetLinkUpdateOptions](../vs140/COleClientItem--GetLinkUpdateOptions.md)   
 [COleLinksDialog Class](../vs140/COleLinksDialog-Class.md)