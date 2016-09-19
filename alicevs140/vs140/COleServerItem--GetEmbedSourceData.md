---
title: "COleServerItem::GetEmbedSourceData"
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
ms.assetid: 9ccee506-30f0-4b08-a9a4-7c7ca6bc3981
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::GetEmbedSourceData
Call this function to get the **CF_EMBEDSOURCE** data for an OLE item.  
  
## Syntax  
  
```  
  
      void GetEmbedSourceData(  
   LPSTGMEDIUM lpStgMedium   
);   
```  
  
#### Parameters  
 `lpStgMedium`  
 Pointer to the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure that will receive the **CF_EMBEDSOURCE** data for the OLE item.  
  
## Remarks  
 This format includes the item's native data. You must have implemented the `Serialize` member function for this function to work properly.  
  
 The result can then be added to a data source by using [COleDataSource::CacheData](../vs140/COleDataSource--CacheData.md). This function is called automatically by [COleServerItem::OnGetClipboardData](../vs140/COleServerItem--OnGetClipboardData.md).  
  
 For more information, see [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::GetLinkSourceData](../vs140/COleServerItem--GetLinkSourceData.md)   
 [COleServerItem::GetObjectDescriptorData](../vs140/COleServerItem--GetObjectDescriptorData.md)   
 [COleDataSource::CacheData](../vs140/COleDataSource--CacheData.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)