---
title: "COleClientItem::Close"
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
ms.assetid: 33e205aa-d72f-428a-b597-9433cf4f8c2a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::Close
Call this function to change the state of an OLE item from the running state to the loaded state, that is, loaded with its handler in memory but with the server not running.  
  
## Syntax  
  
```  
  
      void Close(  
   OLECLOSE dwCloseOption = OLECLOSE_SAVEIFDIRTY   
);  
```  
  
#### Parameters  
 `dwCloseOption`  
 Flag specifying under what circumstances the OLE item is saved when it returns to the loaded state. It can have one of the following values:  
  
-   `OLECLOSE_SAVEIFDIRTY` Save the OLE item.  
  
-   `OLECLOSE_NOSAVE` Do not save the OLE item.  
  
-   `OLECLOSE_PROMPTSAVE` Prompt the user on whether to save the OLE item.  
  
## Remarks  
 This function has no effect when the OLE item is not running.  
  
 For more information, see [IOleObject::Close](http://msdn.microsoft.com/library/windows/desktop/ms683922) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::UpdateLink](../vs140/COleClientItem--UpdateLink.md)