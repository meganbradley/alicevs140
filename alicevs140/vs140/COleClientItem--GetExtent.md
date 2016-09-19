---
title: "COleClientItem::GetExtent"
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
ms.assetid: 3e0f3748-99bb-4bb4-a84f-2bf521eb31e4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetExtent
Call this function to retrieve the OLE item's size.  
  
## Syntax  
  
```  
  
      BOOL GetExtent(  
   LPSIZE lpSize,  
   DVASPECT nDrawAspect = (DVASPECT  
)-1   
);  
```  
  
#### Parameters  
 `lpSize`  
 Pointer to a **SIZE** structure or a `CSize` object that will receive the size information.  
  
 `nDrawAspect`  
 Specifies the aspect of the OLE item whose bounds are to be retrieved. For possible values, see [SetDrawAspect](../vs140/COleClientItem--SetDrawAspect.md).  
  
## Return Value  
 Nonzero if successful; 0 if the OLE item is blank.  
  
## Remarks  
 If the server application was written using the Microsoft Foundation Class Library, this function causes the [OnGetExtent](../vs140/COleServerItem--OnGetExtent.md) member function of the corresponding `COleServerItem` object to be called. Note that the retrieved size may differ from the size last set by the [SetExtent](../vs140/COleClientItem--SetExtent.md) member function; the size specified by `SetExtent` is treated as a suggestion. The dimensions are in `MM_HIMETRIC` units.  
  
> [!NOTE]
>  Do not call `GetExtent` during the processing of an OLE handler, such as [OnChange](../vs140/COleClientItem--OnChange.md). Call [GetCachedExtent](../vs140/COleClientItem--GetCachedExtent.md) instead.  
  
 For more information, see [IOleObject::GetExtent](http://msdn.microsoft.com/library/windows/desktop/ms692325) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::SetExtent](../vs140/COleClientItem--SetExtent.md)   
 [COleClientItem::GetCachedExtent](../vs140/COleClientItem--GetCachedExtent.md)   
 [COleServerItem::OnGetExtent](../vs140/COleServerItem--OnGetExtent.md)