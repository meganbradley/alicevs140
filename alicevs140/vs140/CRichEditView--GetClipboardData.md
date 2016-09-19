---
title: "CRichEditView::GetClipboardData"
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
ms.assetid: 3dfc2da1-5603-4df5-ab7f-03a4d55de1cf
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetClipboardData
The framework calls this function as part of the processing of [IRichEditOleCallback::GetClipboardData](http://msdn.microsoft.com/library/windows/desktop/bb774315).  
  
## Syntax  
  
```  
  
      virtual HRESULT GetClipboardData(  
   CHARRANGE* lpchrg,  
   DWORD dwReco,  
   LPDATAOBJECT lpRichDataObj,  
   LPDATAOBJECT* lplpdataobj   
);  
```  
  
#### Parameters  
 `lpchrg`  
 Pointer to the [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure specifying the range of characters (and OLE items) to copy to the data object specified by `lplpdataobj`.  
  
 `dwReco`  
 Clipboard operation flag. Can be one of these values.  
  
-   **RECO_COPY** Copy to the Clipboard.  
  
-   **RECO_CUT** Cut to the Clipboard.  
  
-   **RECO_DRAG** Drag operation (drag and drop).  
  
-   **RECO_DROP** Drop operation (drag and drop).  
  
-   **RECO_PASTE** Paste from the Clipboard.  
  
 `lpRichDataObj`  
 Pointer to an [IDataObject](http://msdn.microsoft.com/library/windows/desktop/ms688421) object containing the Clipboard data from the rich edit control ([IRichEditOle::GetClipboardData](http://msdn.microsoft.com/library/windows/desktop/bb774341)).  
  
 `lplpdataobj`  
 Pointer to the pointer variable that receives the address of the `IDataObject` object representing the range specified in the `lpchrg` parameter. The value of `lplpdataobj` is ignored if an error is returned.  
  
## Return Value  
 An `HRESULT` value reporting the success of the operation. For more information on `HRESULT`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If the return value indicates success, **IRichEditOleCallback::GetClipboardData** returns the `IDataObject` accessed by `lplpdataobj`; otherwise, it returns the one accessed by `lpRichDataObj`. Override this function to supply your own Clipboard data. The default implementation of this function returns **E_NOTIMPL**.  
  
 This is an advanced overridable.  
  
 For more information, see [IRichEditOle::GetClipboardData](http://msdn.microsoft.com/library/windows/desktop/bb774341), [IRichEditOleCallback::GetClipboardData](http://msdn.microsoft.com/library/windows/desktop/bb774315), and [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] and see [IDataObject](http://msdn.microsoft.com/library/windows/desktop/ms688421) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::GetClipboardData](../vs140/COleServerItem--GetClipboardData.md)