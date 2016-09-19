---
title: "CMFCDragFrameImpl Class"
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
ms.assetid: 500cd824-8188-43c2-8754-b7bb46b5648a
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDragFrameImpl Class
The `CMFCDragFrameImpl` class draws the drag rectangle that appears when the user drags a pane in the standard dock mode.  
  
## Syntax  
  
```  
class CMFCDragFrameImpl  
```  
  
## Remarks  
 An object of this class is embedded in each [CPane](../vs140/CPane-Class.md) object. Thus, each pane that uses the `CanFloat` method displays a drag rectangle when the user drags it.  
  
 You can control the thickness of the drag rectangle by using [GLOBAL_DATA::m_nDragFrameThicknessFloat](../vs140/AFX_GLOBAL_DATA--m_nDragFrameThicknessFloat.md) and [GLOBAL_DATA::m_nDragFrameThicknessDock](../vs140/AFX_GLOBAL_DATA--m_nDragFrameThicknessDock.md).  
  
## Inheritance Hierarchy  
 [CMFCDragFrameImpl](../vs140/CMFCDragFrameImpl-Class.md)  
  
## Requirements  
 **Header:** afxdragframeimpl.h  
  
##  <a name="cmfcdragframeimpl__enddrawdragframe"></a>  CMFCDragFrameImpl::EndDrawDragFrame  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void EndDrawDragFrame(  
   BOOL bClearInternalRects = TRUE  
);  
```  
  
### Parameters  
 [in] `bClearInternalRects`  
  
### Remarks  
  
##  <a name="cmfcdragframeimpl__init"></a>  CMFCDragFrameImpl::Init  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void Init(  
   CWnd* pDraggedWnd  
);  
```  
  
### Parameters  
 [in] `pDraggedWnd`  
  
### Remarks  
  
##  <a name="cmfcdragframeimpl__movedragframe"></a>  CMFCDragFrameImpl::MoveDragFrame  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void MoveDragFrame(  
   BOOL bForceMove = FALSE  
);  
```  
  
### Parameters  
 [in] `bForceMove`  
  
### Remarks  
  
##  <a name="cmfcdragframeimpl__placetabpredocking"></a>  CMFCDragFrameImpl::PlaceTabPreDocking  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void PlaceTabPreDocking(  
   CBaseTabbedPane* pTabbedBar,  
   BOOL bFirstTime  
);  
void PlaceTabPreDocking(  
   CWnd* pCBarToPlaceOn  
);  
```  
  
### Parameters  
 [in] `pTabbedBar`  
  [in] `bFirstTime`  
  [in] `pCBarToPlaceOn`  
  
### Remarks  
  
##  <a name="cmfcdragframeimpl__removetabpredocking"></a>  CMFCDragFrameImpl::RemoveTabPreDocking  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void RemoveTabPreDocking(  
   CDockablePane* pOldTargetBar = NULL  
);  
```  
  
### Parameters  
 [in] `pOldTargetBar`  
  
### Remarks  
  
##  <a name="cmfcdragframeimpl__resetstate"></a>  CMFCDragFrameImpl::ResetState  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void ResetState();  
```  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CPane](../vs140/CPane-Class.md)   
 [GLOBAL_DATA::m_nDragFrameThicknessFloat](../vs140/AFX_GLOBAL_DATA--m_nDragFrameThicknessFloat.md)   
 [GLOBAL_DATA::m_nDragFrameThicknessDock](../vs140/AFX_GLOBAL_DATA--m_nDragFrameThicknessDock.md)