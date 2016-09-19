---
title: "COleServerItem::OnSetData"
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
ms.assetid: 7a83f950-f00f-42a8-9e52-ca8fbd13704e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnSetData
Called by the framework to replace the OLE item's data with the specified data.  
  
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
 Pointer to a [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure specifying the format of the data.  
  
 `lpStgMedium`  
 Pointer to a [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812) structure in which the data resides.  
  
 `bRelease`  
 Indicates who has ownership of the storage medium after completing the function call. The caller decides who is responsible for releasing the resources allocated on behalf of the storage medium. The caller does this by setting `bRelease`. If `bRelease` is nonzero, the server item takes ownership, freeing the medium when it has finished using it. When `bRelease` is 0, the caller retains ownership and the server item can use the storage medium only for the duration of the call.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The server item does not take ownership of the data until it has successfully obtained it. That is, it does not take ownership if it returns 0. If the data source takes ownership, it frees the storage medium by calling the [ReleaseStgMedium](http://msdn.microsoft.com/library/windows/desktop/ms693491) function.  
  
 The default implementation does nothing. Override this function to replace the OLE item's data with the specified data. This is an advanced overridable.  
  
 For more information, see [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812), [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177), and [ReleaseStgMedium](http://msdn.microsoft.com/library/windows/desktop/ms693491) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::OnSetData](../vs140/COleDataSource--OnSetData.md)