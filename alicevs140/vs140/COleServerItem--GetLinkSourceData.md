---
title: "COleServerItem::GetLinkSourceData"
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
ms.assetid: 3888d18e-550f-44b7-9471-930d0374fe0a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::GetLinkSourceData
Call this function to get the `CF_LINKSOURCE` data for an OLE item.  
  
## Syntax  
  
```  
  
      BOOL GetLinkSourceData(  
   LPSTGMEDIUM lpStgMedium   
);  
```  
  
#### Parameters  
 `lpStgMedium`  
 Pointer to the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure that will receive the `CF_LINKSOURCE` data for the OLE item.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This format includes the CLSID describing the type of the OLE item and the information needed to locate the document containing the OLE item.  
  
 The result can then be added to a data source with [COleDataSource::CacheData](../vs140/COleDataSource--CacheData.md). This function is called automatically by [OnGetClipboardData](../vs140/COleServerItem--OnGetClipboardData.md).  
  
 For more information, see [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::GetEmbedSourceData](../vs140/COleServerItem--GetEmbedSourceData.md)   
 [COleServerItem::GetObjectDescriptorData](../vs140/COleServerItem--GetObjectDescriptorData.md)