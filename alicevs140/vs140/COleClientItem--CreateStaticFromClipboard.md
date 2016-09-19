---
title: "COleClientItem::CreateStaticFromClipboard"
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
ms.assetid: a15689d9-5a07-43d5-b950-368057b273cc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::CreateStaticFromClipboard
Call this function to create a static item from the contents of the Clipboard.  
  
## Syntax  
  
```  
  
      BOOL CreateStaticFromClipboard(  
   OLERENDER render = OLERENDER_DRAW,  
   CLIPFORMAT cfFormat = 0,  
   LPFORMATETC lpFormatEtc = NULL   
);  
```  
  
#### Parameters  
 *render*  
 Flag specifying how the server will render the OLE item. For the possible values, see [OLERENDER](http://msdn.microsoft.com/library/windows/desktop/ms691507) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `cfFormat`  
 Specifies the Clipboard data format to be cached when creating the OLE item.  
  
 `lpFormatEtc`  
 Pointer to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure used if *render* is **OLERENDER_FORMAT** or **OLERENDER_DRAW**. Provide a value for this parameter only if you want to specify additional format information beyond the Clipboard format specified by `cfFormat`. If you omit this parameter, default values are used for the other fields in the **FORMATETC** structure.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 A static item contains the presentation data but not the native data; consequently it cannot be edited. You typically call this function if the [CreateFromClipboard](../vs140/COleClientItem--CreateFromClipboard.md) member function fails.  
  
 For more information, see [OLERENDER](http://msdn.microsoft.com/library/windows/desktop/ms691507) and [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::AttachClipboard](../vs140/COleDataObject--AttachClipboard.md)   
 [COleClientItem::CanPaste](../vs140/COleClientItem--CanPaste.md)   
 [COleClientItem::CreateStaticFromData](../vs140/COleClientItem--CreateStaticFromData.md)