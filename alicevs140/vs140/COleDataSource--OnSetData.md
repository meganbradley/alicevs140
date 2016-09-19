---
title: "COleDataSource::OnSetData"
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
ms.assetid: 65ef3be5-f152-4d94-a6b0-600836e09f61
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::OnSetData
Called by the framework to set or replace the data in the `COleDataSource` object in the specified format.  
  
## Syntax  
  
```  
  
      virtual BOOL OnSetData(  
   LPFORMATETC lpFormatEtc,  
   LPSTGMEDIUM lpStgMedium,  
   BOOL bRelease   
);  
```  
  
#### Parameters  
 `lpFormatEtc`  
 Points to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure specifying the format in which data is being replaced.  
  
 `lpStgMedium`  
 Points to the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure containing the data that will replace the current contents of the `COleDataSource` object.  
  
 `bRelease`  
 Indicates who has ownership of the storage medium after completing the function call. The caller decides who is responsible for releasing the resources allocated on behalf of the storage medium. The caller does this by setting `bRelease`. If `bRelease` is nonzero, the data source takes ownership, freeing the medium when it has finished using it. When `bRelease` is 0, the caller retains ownership and the data source can use the storage medium only for the duration of the call.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The data source does not take ownership of the data until it has successfully obtained it. That is, it does not take ownership if `OnSetData` returns 0. If the data source takes ownership, it frees the storage medium by calling the [ReleaseStgMedium](http://msdn.microsoft.com/library/windows/desktop/ms693491) function.  
  
 The default implementation does nothing. Override this function to replace the data in the specified format. This is an advanced overridable.  
  
 For more information, see the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) and [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structures and the [ReleaseStgMedium](http://msdn.microsoft.com/library/windows/desktop/ms693491) and [IDataObject::GetData](http://msdn.microsoft.com/library/windows/desktop/ms678431) functions in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::DelaySetData](../vs140/COleDataSource--DelaySetData.md)   
 [COleDataSource::OnRenderData](../vs140/COleDataSource--OnRenderData.md)   
 [COleDataSource::OnRenderFileData](../vs140/COleDataSource--OnRenderFileData.md)   
 [COleDataSource::OnRenderGlobalData](../vs140/COleDataSource--OnRenderGlobalData.md)   
 [COleServerItem::OnSetData](../vs140/COleServerItem--OnSetData.md)