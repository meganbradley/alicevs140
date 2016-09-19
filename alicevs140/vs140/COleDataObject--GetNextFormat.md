---
title: "COleDataObject::GetNextFormat"
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
ms.assetid: 89f630d2-193e-41f7-9ab9-2355943d3381
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::GetNextFormat
Call this function repeatedly to obtain all the formats available for retrieving data from the item.  
  
## Syntax  
  
```  
  
      BOOL GetNextFormat(  
   LPFORMATETC lpFormatEtc   
);   
```  
  
#### Parameters  
 `lpFormatEtc`  
 Points to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure that receives the format information when the function call returns.  
  
## Return Value  
 Nonzero if another format is available; otherwise 0.  
  
## Remarks  
 After a call to [COleDataObject::BeginEnumFormats](../vs140/COleDataObject--BeginEnumFormats.md), the position of the first format supported by this data object is stored. Successive calls to `GetNextFormat` will enumerate the list of available formats in the data object. Use these functions to list the available formats.  
  
 To check for the availability of a given format, call [COleDataObject::IsDataAvailable](../vs140/COleDataObject--IsDataAvailable.md).  
  
 For more information, see [IEnumXXXX::Next](https://msdn.microsoft.com/en-us/library/ms695273.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::BeginEnumFormats](../vs140/COleDataObject--BeginEnumFormats.md)   
 [COleDataObject::GetData](../vs140/COleDataObject--GetData.md)   
 [COleDataObject::GetFileData](../vs140/COleDataObject--GetFileData.md)   
 [COleDataObject::GetGlobalData](../vs140/COleDataObject--GetGlobalData.md)