---
title: "CRecentDockSiteInfo Class"
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
ms.assetid: 2dd14f95-d5a2-4461-a7a5-2c6c36a3a165
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecentDockSiteInfo Class
The `CRecentDockSiteInfo` class is a helper class that stores recent state information for the [CPane Class](../vs140/CPane-Class.md).  
  
## Syntax  
  
```  
class CRecentDockSiteInfo : public CObject  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`CRecentDockSiteInfo::CRecentDockSiteInfo`|Default constructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CRecentDockSiteInfo::CleanUp](#crecentdocksiteinfo__cleanup)||  
|[CRecentDockSiteInfo::GetRecentDefaultPaneDivider](#crecentdocksiteinfo__getrecentdefaultpanedivider)||  
|[CRecentDockSiteInfo::GetRecentDockedPercent](#crecentdocksiteinfo__getrecentdockedpercent)||  
|[CRecentDockSiteInfo::GetRecentDockedRect](#crecentdocksiteinfo__getrecentdockedrect)||  
|[CRecentDockSiteInfo::GetRecentListOfPanes](#crecentdocksiteinfo__getrecentlistofpanes)||  
|[CRecentDockSiteInfo::GetRecentPaneContainer](#crecentdocksiteinfo__getrecentpanecontainer)||  
|[CRecentDockSiteInfo::GetRecentTabContainer](#crecentdocksiteinfo__getrecenttabcontainer)||  
|[CRecentDockSiteInfo::Init](#crecentdocksiteinfo__init)||  
|[CRecentDockSiteInfo::IsRecentLeftPane](#crecentdocksiteinfo__isrecentleftpane)||  
|[CRecentDockSiteInfo::operator=](#crecentdocksiteinfo__operator__eq)||  
|[CRecentDockSiteInfo::SaveListOfRecentPanes](#crecentdocksiteinfo__savelistofrecentpanes)||  
|[CRecentDockSiteInfo::SetInfo](#crecentdocksiteinfo__setinfo)||  
|[CRecentDockSiteInfo::StoreDockInfo](#crecentdocksiteinfo__storedockinfo)||  
  
## Remarks  
 The `CRecentDockSiteInfo` class is a data management class. It tracks the last state of a `CPane` as it transitions between being docked and floating. When a user double clicks a floating dockable pane, it becomes docked. Double clicking the docked pane returns it to its previous location, size, and state. Similarly, when the pane is re-docked it returns to its previous docking location. This data class is what makes that possible. Since the members of this class store state information for the docked pane, they should not be directly modified by your application.  
  
 A `CRecentDockSiteInfo` object is created every time that a pane is created. Each `CPane` object has a member variable, [CPane::m_recentDockInfo](../vs140/CPane-Class.md#cpane__m_recentdockinfo), to store this information.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CRecentDockSiteInfo](../vs140/CRecentDockSiteInfo-Class.md)  
  
## Requirements  
 **Header:** afxrecentDockSiteInfo.h  
  
##  <a name="crecentdocksiteinfo__cleanup"></a>  CRecentDockSiteInfo::CleanUp  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void CleanUp();  
```  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__crecentdocksiteinfo"></a>  CRecentDockSiteInfo::CRecentDockSiteInfo  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CRecentDockSiteInfo(  
   CPane* pBar  
);  
```  
  
### Parameters  
 [in] `pBar`  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__getrecentdefaultpanedivider"></a>  CRecentDockSiteInfo::GetRecentDefaultPaneDivider  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CPaneDivider* GetRecentDefaultPaneDivider();  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__getrecentdockedpercent"></a>  CRecentDockSiteInfo::GetRecentDockedPercent  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
int GetRecentDockedPercent(  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__getrecentdockedrect"></a>  CRecentDockSiteInfo::GetRecentDockedRect  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CRect& GetRecentDockedRect(  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__getrecentlistofpanes"></a>  CRecentDockSiteInfo::GetRecentListOfPanes  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CList<HWND, HWND>& GetRecentListOfPanes(  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__getrecentpanecontainer"></a>  CRecentDockSiteInfo::GetRecentPaneContainer  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CPaneContainer* GetRecentPaneContainer(  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__getrecenttabcontainer"></a>  CRecentDockSiteInfo::GetRecentTabContainer  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CPaneContainer* GetRecentTabContainer(  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__init"></a>  CRecentDockSiteInfo::Init  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void Init();  
```  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__isrecentleftpane"></a>  CRecentDockSiteInfo::IsRecentLeftPane  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
BOOL IsRecentLeftPane(  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__operator__eq"></a>  CRecentDockSiteInfo::operator =  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CRecentDockSiteInfo& operator=(  
   CRecentDockSiteInfo& src  
);  
```  
  
### Parameters  
 [in] `src`  
  
### Return Value  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__savelistofrecentpanes"></a>  CRecentDockSiteInfo::SaveListOfRecentPanes  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
void SaveListOfRecentPanes( CList<HWND,  
   HWND>& lstOrg,  
   BOOL bForSlider  
);  
```  
  
### Parameters  
 [in] `CList<HWND`  
  [in] `lstOrg`  
  [in] `bForSlider`  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__setinfo"></a>  CRecentDockSiteInfo::SetInfo  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void SetInfo(  
   BOOL bForSlider,  
   CRecentDockSiteInfo& srcInfo  
);  
```  
  
### Parameters  
 [in] `bForSlider`  
  [in] `srcInfo`  
  
### Remarks  
  
##  <a name="crecentdocksiteinfo__storedockinfo"></a>  CRecentDockSiteInfo::StoreDockInfo  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
virtual void StoreDockInfo(  
   CPaneContainer* pRecentContainer,  
   CDockablePane* pTabbedBar = NULL  
);  
```  
  
### Parameters  
 [in] `pRecentContainer`  
  [in] `pTabbedBar`  
  
### Remarks  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CDockSite Class](../vs140/CDockSite-Class.md)