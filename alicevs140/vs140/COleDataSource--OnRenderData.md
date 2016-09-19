---
title: "COleDataSource::OnRenderData"
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
ms.assetid: 3b82e777-bcc4-4145-a4e0-125b65a6b3ba
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::OnRenderData
Called by the framework to retrieve data in the specified format.  
  
## Syntax  
  
```  
  
      virtual BOOL OnRenderData(  
   LPFORMATETC lpFormatEtc,  
   LPSTGMEDIUM lpStgMedium   
);  
```  
  
#### Parameters  
 `lpFormatEtc`  
 Points to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure specifying the format in which information is requested.  
  
 `lpStgMedium`  
 Points to a [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure in which the data is to be returned.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The specified format is one previously placed in the `COleDataSource` object using the [DelayRenderData](../vs140/COleDataSource--DelayRenderData.md) or [DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md) member function for delayed rendering. The default implementation of this function will call [OnRenderFileData](../vs140/COleDataSource--OnRenderFileData.md) or [OnRenderGlobalData](../vs140/COleDataSource--OnRenderGlobalData.md) if the supplied storage medium is either a file or memory, respectively. If neither of these formats are supplied, then the default implementation will return 0 and do nothing. For more information on delayed rendering as handled by MFC, see the article [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md).  
  
 If `lpStgMedium`->*tymed* is **TYMED_NULL**, the **STGMEDIUM** should be allocated and filled as specified by *lpFormatEtc->tymed*. If it is not **TYMED_NULL**, the **STGMEDIUM** should be filled in place with the data.  
  
 This is an advanced overridable. Override this function to supply your data in the requested format and medium. Depending on your data, you may want to override one of the other versions of this function instead. If your data is small and fixed in size, override `OnRenderGlobalData`. If your data is in a file, or is of variable size, override `OnRenderFileData`.  
  
 For more information, see the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) and [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structures, the [TYMED](http://msdn.microsoft.com/library/windows/desktop/ms691227) enumeration type, and [IDataObject::GetData](http://msdn.microsoft.com/library/windows/desktop/ms678431) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::DelayRenderData](../vs140/COleDataSource--DelayRenderData.md)   
 [COleDataSource::DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md)   
 [COleDataSource::OnRenderFileData](../vs140/COleDataSource--OnRenderFileData.md)   
 [COleDataSource::OnRenderGlobalData](../vs140/COleDataSource--OnRenderGlobalData.md)   
 [COleDataSource::OnSetData](../vs140/COleDataSource--OnSetData.md)