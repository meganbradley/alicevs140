---
title: "COleClientItem::Release"
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
ms.assetid: 5e895c84-b4af-4cef-a307-b82e0f523ad3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::Release
Call this function to clean up resources used by the OLE item.  
  
## Syntax  
  
```  
  
      virtual void Release(  
   OLECLOSE dwCloseOption = OLECLOSE_NOSAVE   
);  
```  
  
#### Parameters  
 `dwCloseOption`  
 Flag specifying under what circumstances the OLE item is saved when it returns to the loaded state. For a list of possible values, see [COleClientItem::Close](../vs140/COleClientItem--Close.md).  
  
## Remarks  
 **Release** is called by the `COleClientItem` destructor.  
  
 For more information, see [IUnknown::Release](http://msdn.microsoft.com/library/windows/desktop/ms682317) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::Close](../vs140/COleClientItem--Close.md)   
 [COleClientItem::Delete](../vs140/COleClientItem--Delete.md)