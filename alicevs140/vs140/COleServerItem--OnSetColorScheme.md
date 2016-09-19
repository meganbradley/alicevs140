---
title: "COleServerItem::OnSetColorScheme"
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
ms.assetid: c0aef3d5-d74b-4e30-a76d-b80b78d745dc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnSetColorScheme
Called by the framework to specify a color palette to be used when editing the OLE item.  
  
## Syntax  
  
```  
  
      virtual BOOL OnSetColorScheme(  
   const LOGPALETTE* lpLogPalette   
);  
```  
  
#### Parameters  
 `lpLogPalette`  
 Pointer to a Windows [LOGPALETTE](http://msdn.microsoft.com/library/windows/desktop/dd145040) structure.  
  
## Return Value  
 Nonzero if the color palette is used; otherwise 0.  
  
## Remarks  
 If the container application was written using the Microsoft Foundation Class Library, this function is called when the [IOleObject::SetColorScheme](http://msdn.microsoft.com/library/windows/desktop/ms683971) function of the corresponding `COleClientItem` object is called. The default implementation returns **FALSE**. Override this function if you want to use the recommended palette. The server application is not required to use the suggested palette.  
  
 For more information, see [IOleObject::SetColorScheme](http://msdn.microsoft.com/library/windows/desktop/ms683971) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)