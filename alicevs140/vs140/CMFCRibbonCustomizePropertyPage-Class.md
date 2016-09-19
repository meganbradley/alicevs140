---
title: "CMFCRibbonCustomizePropertyPage Class"
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
ms.assetid: ea32a99a-dfbe-401e-8975-aa191552532f
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCustomizePropertyPage Class
Implements a custom page for the **Customize** dialog box in Ribbon-based applications.  
  
## Syntax  
  
```  
class CMFCRibbonCustomizePropertyPage: public CMFCPropertyPage  
```  
  
## Members  
  
### Public Constructors  
  
|||  
|-|-|  
|Name|Description|  
|[CMFCRibbonCustomizePropertyPage::CMFCRibbonCustomizePropertyPage](#cmfcribboncustomizepropertypage__cmfcribboncustomizepropertypage)|Constructs a `CMFCRibbonCustomizePropertyPage` object.|  
|`CMFCRibbonCustomizePropertyPage::~CMFCRibbonCustomizePropertyPage`|Destructor.|  
  
### Public Methods  
  
|||  
|-|-|  
|Name|Description|  
|[CMFCRibbonCustomizePropertyPage::AddCustomCategory](#cmfcribboncustomizepropertypage__addcustomcategory)|Adds a custom category to the **Commands** combo box.|  
|`CMFCRibbonCustomizePropertyPage::CreateObject`|Used by the framework to create a dynamic instance of this class type.|  
|`CMFCRibbonCustomizePropertyPage::GetThisClass`|Used by the framework to obtain a pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) object that is associated with this class type.|  
|[CMFCRibbonCustomizePropertyPage::OnOK](#cmfcribboncustomizepropertypage__onok)|Called by the system when a user clicks **OK** on the **Customize** dialog box.|  
  
## Remarks  
 If you want to add custom commands to the **Customize** dialog box, you must handle the AFX_WM_ON_RIBBON_CUSTOMIZE message. In the message handler, instantiate a `CMFCRibbonCustomizePropertyPage` object on the stack. Create a list of custom commands, and then call `AddCustomCategory` to add the new page to the **Customize** dialog box.  
  
## Example  
 The following example demonstrates how to construct a `CMFCRibbonCustomizePropertyPage` object and to add a custom category.  
  
 [!CODE [NVC_MFC_RibbonApp#22](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#22)]  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CPropertyPage](../vs140/CPropertyPage-Class.md)  
  
 [CMFCPropertyPage](../vs140/CMFCPropertyPage-Class.md)  
  
 [CMFCRibbonCustomizePropertyPage](../vs140/CMFCRibbonCustomizePropertyPage-Class.md)  
  
## Requirements  
 **Header:** afxribboncustomizedialog.h  
  
##  <a name="cmfcribboncustomizepropertypage__addcustomcategory"></a>  CMFCRibbonCustomizePropertyPage::AddCustomCategory  
 Adds a custom category to the **Commands** combo box.  
  
```  
void AddCustomCategory(  
   LPCTSTR lpszName,  
   const CList<UINT, UINT>& lstIDS  
);  
```  
  
### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `lpszName`|Specifies the custom category name.|  
|[in] `lstIDS`|Contains ribbon command IDs to be shown in the custom category.|  
  
### Remarks  
 This method adds a category named `lpszName` to the **Commands** combo box. When the user selects the category, the commands specified in `lstIDS` appear in the command list.  
  
##  <a name="cmfcribboncustomizepropertypage__cmfcribboncustomizepropertypage"></a>  CMFCRibbonCustomizePropertyPage::CMFCRibbonCustomizePropertyPage  
 Constructs a `CMFCRibbonCustomizePropertyPage` object.  
  
```  
CMFCRibbonCustomizePropertyPage(  
   CMFCRibbonBar* pRibbonBar = NULL  
);  
```  
  
### Parameters  
 [in] `pRibbonBar`  
 A pointer to a ribbon control for which the options to customize.  
  
##  <a name="cmfcribboncustomizepropertypage__onok"></a>  CMFCRibbonCustomizePropertyPage::OnOK  
 Calleld by the system when a user clicks **OK** on the **Customize** dialog box.  
  
```  
virtual void OnOK();  
```  
  
### Remarks  
 The default implementation applies the options selected in the **Customize** dialog box to the Quick Access Toolbar.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)