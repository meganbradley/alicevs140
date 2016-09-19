---
title: "COleDataObject::BeginEnumFormats"
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
ms.assetid: 5706ad4a-9ed1-40d0-ba56-66f610f109d7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataObject::BeginEnumFormats
Call this function to prepare for subsequent calls to `GetNextFormat` for retrieving a list of data formats from the item.  
  
## Syntax  
  
```  
  
void BeginEnumFormats( );  
```  
  
## Remarks  
 After a call to `BeginEnumFormats`, the position of the first format supported by this data object is stored. Successive calls to `GetNextFormat` will enumerate the list of available formats in the data object.  
  
 To check on the availability of data in a given format, use [COleDataObject::IsDataAvailable](../vs140/COleDataObject--IsDataAvailable.md).  
  
 For more information, see [IDataObject::EnumFormatEtc](http://msdn.microsoft.com/library/windows/desktop/ms683979) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject::GetNextFormat](../vs140/COleDataObject--GetNextFormat.md)   
 [COleDataObject::IsDataAvailable](../vs140/COleDataObject--IsDataAvailable.md)