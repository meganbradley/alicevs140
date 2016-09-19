---
title: "COleDataSource::CacheData"
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
ms.assetid: c8ee2117-390f-47d7-b002-83625797cb67
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::CacheData
Call this function to specify a format in which data is offered during data transfer operations.  
  
## Syntax  
  
```  
  
      void CacheData(  
   CLIPFORMAT cfFormat,  
   LPSTGMEDIUM lpStgMedium,  
   LPFORMATETC lpFormatEtc = NULL   
);  
```  
  
#### Parameters  
 `cfFormat`  
 The Clipboard format in which the data is to be offered. This parameter can be one of the predefined Clipboard formats or the value returned by the native Windows [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) function.  
  
 `lpStgMedium`  
 Points to a [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure containing the data in the format specified.  
  
 `lpFormatEtc`  
 Points to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure describing the format in which the data is to be offered. Provide a value for this parameter if you want to specify additional format information beyond the Clipboard format specified by `cfFormat`. If it is **NULL**, default values are used for the other fields in the **FORMATETC** structure.  
  
## Remarks  
 You must supply the data, because this function provides it by using immediate rendering. The data is cached until needed.  
  
 Supply the data using a [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure. You can also use the `CacheGlobalData` member function if the amount of data you are supplying is small enough to be transferred efficiently using an `HGLOBAL`.  
  
 After the call to `CacheData` the **ptd** member of `lpFormatEtc` and the contents of `lpStgMedium` are owned by the data object, not by the caller.  
  
 To use delayed rendering, call the [DelayRenderData](../vs140/COleDataSource--DelayRenderData.md) or [DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md) member function. For more information on delayed rendering as handled by MFC, see the article [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md).  
  
 For more information, see the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) and [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structures in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 For more information, see [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::CacheGlobalData](../vs140/COleDataSource--CacheGlobalData.md)   
 [COleDataSource::DelayRenderData](../vs140/COleDataSource--DelayRenderData.md)   
 [COleDataSource::DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)   
 [COleDataSource::DoDragDrop](../vs140/COleDataSource--DoDragDrop.md)