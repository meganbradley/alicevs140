---
title: "CMFCRibbonMainPanel Class"
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
ms.assetid: 1af78798-5e75-4365-9c81-a54aa5679602
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonMainPanel Class
Implements a ribbon panel that displays when you click the [CMFCRibbonApplicationButton](../vs140/CMFCRibbonApplicationButton-Class.md).  
  
## Syntax  
  
```  
class CMFCRibbonMainPanel : public CMFCRibbonPanel  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`CMFCRibbonMainPanel::CMFCRibbonMainPanel`|Default constructor.|  
|`CMFCRibbonMainPanel::~CMFCRibbonMainPanel`|Destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCRibbonMainPanel::Add](#cmfcribbonmainpanel__add)|Adds a ribbon element to the left pane of the application button panel. (Overrides [CMFCRibbonPanel::Add](../vs140/CMFCRibbonPanel-Class.md#cmfcribbonpanel__add).)|  
|[CMFCRibbonMainPanel::AddRecentFilesList](#cmfcribbonmainpanel__addrecentfileslist)|Adds a text string to the recent files list menu.|  
|[CMFCRibbonMainPanel::AddToBottom](#cmfcribbonmainpanel__addtobottom)|Adds a ribbon element to the bottom pane of the ribbon application panel.|  
|[CMFCRibbonMainPanel::AddToRight](#cmfcribbonmainpanel__addtoright)|Adds a ribbon element to the right pane of the application button panel.|  
|`CMFCRibbonMainPanel::CreateObject`|Used by the framework to create a dynamic instance of this class type.|  
|[CMFCRibbonMainPanel::GetCommandsFrame](#cmfcribbonmainpanel__getcommandsframe)|Returns a rectangle that represents the area of the ribbon main panel.|  
|`CMFCRibbonMainPanel::GetThisClass`|Used by the framework to obtain a pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) object that is associated with this class type.|  
  
## Remarks  
 The framework displays the `CMFCRibbonMainPanel` when you open the application panel. It contains three panes:  
  
-   The left pane contains commands associated with files, such as **Open**, **Save**, **Print**, and **Close**. To add a command to this pane, call [CMFCRibbonMainPanel::Add](#cmfcribbonmainpanel__add).  
  
-   The right pane contains options that modify the command that you click in the left pane. For example, if you click **Save As** from the left pane, the right pane can display available file types. To add an item to this pane, call [CMFCRibbonMainPanel::AddToRight](#cmfcribbonmainpanel__addtoright).  
  
-   The bottom pane contains buttons that allow you to change the application's settings and to exit the program. To add an item to this pane, call [CMFCRibbonMainPanel::AddToBottom](#cmfcribbonmainpanel__addtobottom).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CMFCRibbonPanel](../vs140/CMFCRibbonPanel-Class.md)  
  
 [CMFCRibbonMainPanel](../vs140/CMFCRibbonMainPanel-Class.md)  
  
## Requirements  
 **Header:** afxRibbonMainPanel.h  
  
##  <a name="cmfcribbonmainpanel__add"></a>  CMFCRibbonMainPanel::Add  
 Adds a ribbon element to the left pane of the application button panel.  
  
```  
virtual void Add(  
    CMFCRibbonBaseElement* pElem   
);  
```  
  
### Parameters  
 [in] [out] `pElem`  
 A pointer to the ribbon element to add to the main panel.  
  
### Remarks  
 Adds a ribbon element to the panel. Elements added using this method will be located in the left column of the main panel.  
  
##  <a name="cmfcribbonmainpanel__addrecentfileslist"></a>  CMFCRibbonMainPanel::AddRecentFilesList  
 Adds a text string to the recent files list menu.  
  
```  
void AddRecentFilesList(  
    LPCTSTR lpszLabel,  
    int nWidth = 300   
);  
```  
  
### Parameters  
 `lpszLabel`  
 Specifies the string to add to the recent files list.  
  
 `nWidth`  
 Specifies the width, in pixels, of the recent files list panel.  
  
### Remarks  
  
##  <a name="cmfcribbonmainpanel__addtobottom"></a>  CMFCRibbonMainPanel::AddToBottom  
 Adds a ribbon element to the bottom pane of the ribbon application panel.  
  
```  
void AddToBottom(  
    CMFCRibbonMainPanelButton* pElem   
);  
```  
  
### Parameters  
 [in] [out] `pElem`  
 A pointer to the ribbon element to add to the bottom of the main panel.  
  
### Remarks  
  
##  <a name="cmfcribbonmainpanel__addtoright"></a>  CMFCRibbonMainPanel::AddToRight  
 Adds a ribbon element to the right pane of the application button panel.  
  
```  
void AddToRight(  
    CMFCRibbonBaseElement* pElem,  
    int nWidth = 300   
);  
```  
  
### Parameters  
 `pElem`  
 A pointer to a ribbon element to be added to the right side of the main panel.  
  
 `nWidth`  
 Specifies the width, in pixels, of the right panel.  
  
### Remarks  
 Use this function to add a ribbon element to the right panel. The right panel typically displays the recent files list, but you can add any other ribbon element here.  
  
##  <a name="cmfcribbonmainpanel__getcommandsframe"></a>  CMFCRibbonMainPanel::GetCommandsFrame  
 Returns a rectangle that represents the area of the ribbon main panel.  
  
```  
CRect GetCommandsFrame() const;  
```  
  
### Return Value  
 A rectangle that represents the area of the ribbon main panel.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)