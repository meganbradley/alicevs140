---
title: "COleDataObject::IsDataAvailable"
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
ms.assetid: 6b0f828f-e92f-4a57-a1ea-20731544b83c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::IsDataAvailable
Call this function to determine if a particular format is available for retrieving data from the OLE item.  
  
## Syntax  
  
```  
  
      BOOL IsDataAvailable(  
   CLIPFORMAT cfFormat,  
   LPFORMATETC lpFormatEtc = NULL   
);  
```  
  
#### Parameters  
 `cfFormat`  
 The Clipboard data format to be used in the structure pointed to by `lpFormatEtc`. This parameter can be one of the predefined Clipboard formats or the value returned by the native Windows [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) function.  
  
 `lpFormatEtc`  
 Points to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure describing the format desired. Provide a value for this parameter only if you want to specify additional format information beyond the Clipboard format specified by `cfFormat`. If it is **NULL**, the default values are used for the other fields in the **FORMATETC** structure.  
  
## Return Value  
 Nonzero if data is available in the specified format; otherwise 0.  
  
## Remarks  
 This function is useful before calling `GetData`, `GetFileData`, or `GetGlobalData`.  
  
 For more information, see [IDataObject::QueryGetData](http://msdn.microsoft.com/library/windows/desktop/ms680637) and [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information, see [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CRichEditView::QueryAcceptData](../vs140/CRichEditView--QueryAcceptData.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::BeginEnumFormats](../vs140/COleDataObject--BeginEnumFormats.md)   
 [COleDataObject::GetData](../vs140/COleDataObject--GetData.md)   
 [COleDataObject::GetFileData](../vs140/COleDataObject--GetFileData.md)   
 [COleDataObject::GetGlobalData](../vs140/COleDataObject--GetGlobalData.md)   
 [COleDataObject::GetNextFormat](../vs140/COleDataObject--GetNextFormat.md)