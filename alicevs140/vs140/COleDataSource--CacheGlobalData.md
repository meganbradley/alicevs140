---
title: "COleDataSource::CacheGlobalData"
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
ms.assetid: 20cfee14-8c75-41f7-a58d-62b50d4c84f3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::CacheGlobalData
Call this function to specify a format in which data is offered during data transfer operations.  
  
## Syntax  
  
```  
  
      void CacheGlobalData(  
   CLIPFORMAT cfFormat,  
   HGLOBAL hGlobal,  
   LPFORMATETC lpFormatEtc = NULL   
);  
```  
  
#### Parameters  
 `cfFormat`  
 The Clipboard format in which the data is to be offered. This parameter can be one of the predefined Clipboard formats or the value returned by the native Windows [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) function.  
  
 *hGlobal*  
 Handle to the global memory block containing the data in the format specified.  
  
 `lpFormatEtc`  
 Points to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure describing the format in which the data is to be offered. Provide a value for this parameter if you want to specify additional format information beyond the Clipboard format specified by `cfFormat`. If it is **NULL**, default values are used for the other fields in the **FORMATETC** structure.  
  
## Remarks  
 This function provides the data using immediate rendering, so you must supply the data when calling the function; the data is cached until needed. Use the `CacheData` member function if you are supplying a large amount of data or if you require a structured storage medium.  
  
 To use delayed rendering, call the [DelayRenderData](../vs140/COleDataSource--DelayRenderData.md) or [DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md) member function. For more information on delayed rendering as handled by MFC, see the article [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md).  
  
 For more information, see the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 For more information, see [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::CacheData](../vs140/COleDataSource--CacheData.md)   
 [COleDataSource::DelayRenderData](../vs140/COleDataSource--DelayRenderData.md)   
 [COleDataSource::DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md)