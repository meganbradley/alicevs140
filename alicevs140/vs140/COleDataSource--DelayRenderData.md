---
title: "COleDataSource::DelayRenderData"
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
ms.assetid: 5ce78993-23d3-413c-afa4-127f9c609fce
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::DelayRenderData
Call this function to specify a format in which data is offered during data transfer operations.  
  
## Syntax  
  
```  
  
      void DelayRenderData(  
   CLIPFORMAT cfFormat,  
   LPFORMATETC lpFormatEtc = NULL   
);  
```  
  
#### Parameters  
 `cfFormat`  
 The Clipboard format in which the data is to be offered. This parameter can be one of the predefined Clipboard formats or the value returned by the native Windows [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) function.  
  
 `lpFormatEtc`  
 Points to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure describing the format in which the data is to be offered. Provide a value for this parameter if you want to specify additional format information beyond the Clipboard format specified by `cfFormat`. If it is **NULL**, default values are used for the other fields in the **FORMATETC** structure.  
  
## Remarks  
 This function provides the data using delayed rendering, so the data is not supplied immediately. The [OnRenderData](../vs140/COleDataSource--OnRenderData.md) or [OnRenderGlobalData](../vs140/COleDataSource--OnRenderGlobalData.md) member function is called to request the data.  
  
 Use this function if you are not going to supply your data through a `CFile` object. If you are going to supply the data through a `CFile` object, call the [DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md) member function. For more information on delayed rendering as handled by MFC, see the article [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md).  
  
 To use immediate rendering, call the [CacheData](../vs140/COleDataSource--CacheData.md) or [CacheGlobalData](../vs140/COleDataSource--CacheGlobalData.md) member function.  
  
 For more information, see the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 For more information, see [RegisterClipboardFormat](http://msdn.microsoft.com/library/windows/desktop/ms649049) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::CacheData](../vs140/COleDataSource--CacheData.md)   
 [COleDataSource::CacheGlobalData](../vs140/COleDataSource--CacheGlobalData.md)   
 [COleDataSource::DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md)   
 [COleDataSource::OnRenderData](../vs140/COleDataSource--OnRenderData.md)   
 [COleDataSource::OnRenderGlobalData](../vs140/COleDataSource--OnRenderGlobalData.md)