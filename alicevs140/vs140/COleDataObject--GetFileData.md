---
title: "COleDataObject::GetFileData"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 9bf5fc2f-297a-4667-ae24-e3ccce5ae00c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::GetFileData
Call this function to create a `CFile` or `CFile`-derived object and to retrieve data in the specified format into a `CFile` pointer.  
  
## Syntax  
  
```  
  
      CFile* GetFileData(  
   CLIPFORMAT cfFormat,  
   LPFORMATETC lpFormatEtc = NULL   
);  
```  
  
#### Parameters  
 `cfFormat`  
 The format in which data is to be returned. This parameter can be one of the predefined Clipboard formats or the value returned by the native Windows [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) function.  
  
 `lpFormatEtc`  
 Points to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure describing the format in which data is to be returned. Provide a value for this parameter if you want to specify additional format information beyond the Clipboard format specified by `cfFormat`. If it is **NULL**, the default values are used for the other fields in the **FORMATETC** structure.  
  
## Return Value  
 Pointer to the new `CFile` or `CFile`-derived object containing the data if successful; otherwise **NULL**.  
  
## Remarks  
 Depending on the medium the data is stored in, the actual type pointed to by the return value may be `CFile`, `CSharedFile`, or `COleStreamFile`.  
  
> [!NOTE]
>  The `CFile` object accessed by the return value of this function is owned by the caller. It is the responsibility of the caller to **delete** the `CFile` object, thereby closing the file.  
  
 For more information, see [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information, see [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::GetData](../vs140/COleDataObject--GetData.md)   
 [COleDataObject::GetGlobalData](../vs140/COleDataObject--GetGlobalData.md)   
 [COleDataObject::IsDataAvailable](../vs140/COleDataObject--IsDataAvailable.md)