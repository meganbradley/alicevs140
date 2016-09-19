---
title: "COleDataSource::OnRenderFileData"
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
ms.assetid: 1ac8edfc-3798-4c4e-bdd0-600b5c70195c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::OnRenderFileData
Called by the framework to retrieve data in the specified format when the specified storage medium is a file.  
  
## Syntax  
  
```  
  
      virtual BOOL OnRenderFileData(  
   LPFORMATETC lpFormatEtc,  
   CFile* pFile   
);  
```  
  
#### Parameters  
 `lpFormatEtc`  
 Points to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure specifying the format in which information is requested.  
  
 `pFile`  
 Points to a [CFile](../vs140/CFile-Class.md) object in which the data is to be rendered.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The specified format is one previously placed in the `COleDataSource` object using the [DelayRenderData](../vs140/COleDataSource--DelayRenderData.md) member function for delayed rendering. The default implementation of this function simply returns **FALSE**.  
  
 This is an advanced overridable. Override this function to supply your data in the requested format and medium. Depending on your data, you might want to override one of the other versions of this function instead. If you want to handle multiple storage media, override [OnRenderData](../vs140/COleDataSource--OnRenderData.md). If your data is in a file, or is of variable size, override `OnRenderFileData`. For more information on delayed rendering as handled by MFC, see the article [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md).  
  
 For more information, see the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure and [IDataObject::GetData](http://msdn.microsoft.com/library/windows/desktop/ms678431) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::DelayRenderData](../vs140/COleDataSource--DelayRenderData.md)   
 [COleDataSource::DelayRenderFileData](../vs140/COleDataSource--DelayRenderFileData.md)   
 [COleDataSource::OnRenderData](../vs140/COleDataSource--OnRenderData.md)   
 [COleDataSource::OnRenderGlobalData](../vs140/COleDataSource--OnRenderGlobalData.md)   
 [COleDataSource::OnSetData](../vs140/COleDataSource--OnSetData.md)   
 [CFile Class](../vs140/CFile-Class.md)