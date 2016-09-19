---
title: "CMFCDesktopAlertWndInfo Class"
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
ms.assetid: 5c9bb84e-6c96-4748-8e74-6951b6ae8e84
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDesktopAlertWndInfo Class
The `CMFCDesktopAlertWndInfo` class is used with the [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md). It specifies the controls that are displayed if the desktop alert window pops up.  
  
## Syntax  
  
```  
class CMFCDesktopAlertWndInfo  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|`CMFCDesktopAlertWndInfo::~CMFCDesktopAlertWndInfo`|Destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCDesktopAlertWndInfo::operator=](#cmfcdesktopalertwndinfo__operator_eq)||  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCDesktopAlertWndInfo::m_hIcon](#cmfcdesktopalertwndinfo__m_hicon)|A handle to the icon that is displayed.|  
|[CMFCDesktopAlertWndInfo::m_nURLCmdID](#cmfcdesktopalertwndinfo__m_nurlcmdid)|The command ID associated with a link on the desktop alert window.|  
|[CMFCDesktopAlertWndInfo::m_strText](#cmfcdesktopalertwndinfo__m_strtext)|The text that is displayed on the desktop alert window.|  
|[CMFCDesktopAlertWndInfo::m_strURL](#cmfcdesktopalertwndinfo__m_strurl)|The link that is displayed on the desktop alert window.|  
  
## Remarks  
 The `CMFCDesktopAlertWndInfo` class is passed to the [CMFCDesktopAlertWnd::Create](../vs140/CMFCDesktopAlertWnd-Class.md#cmfcdesktopalertwnd__create) method to specify the elements that are displayed on the default dialog of the desktop alert window. The default dialog can contain three items:  
  
-   An icon, which is set by calling [CMFCDesktopAlertWndInfo::m_hIcon](#cmfcdesktopalertwndinfo__m_hicon).  
  
-   A label, or text message, which is set by calling [CMFCDesktopAlertWndInfo::m_strText](#cmfcdesktopalertwndinfo__m_strtext).  
  
-   A link, which is set by calling [CMFCDesktopAlertWndInfo::m_strURL](#cmfcdesktopalertwndinfo__m_strurl). To set the command that is executed when the link is clicked, call [CMFCDesktopAlertWndInfo::m_nURLCmdID](#cmfcdesktopalertwndinfo__m_nurlcmdid).  
  
 If the default dialog is not sufficient, you can create a custom dialog and pass it to the [CMFCDesktopAlertWnd::Create](../vs140/CMFCDesktopAlertWnd-Class.md#cmfcdesktopalertwnd__create) method instead of using this class. For more information, see [CMFCDesktopAlertDialog Class](../vs140/CMFCDesktopAlertDialog-Class.md).  
  
## Example  
 The following example demonstrates how to use various members in the `CMFCDesktopAlertWndInfo` class. The example demonstrates how to set the handle to the icon that is displayed, the text that is displayed on the desktop alert window, the link that is displayed on the desktop alert window, and the command ID that is associated with a link on the desktop alert window. This example is part of the [Desktop Alert Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_DesktopAlertDemo#3](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_DesktopAlertDemo#3)]  
  
## Inheritance Hierarchy  
 [CMFCDesktopAlertWndInfo](../vs140/CMFCDesktopAlertWndInfo-Class.md)  
  
## Requirements  
 **Header:** afxDesktopAlertDialog.h  
  
##  <a name="cmfcdesktopalertwndinfo__operator_eq"></a>  CMFCDesktopAlertWndInfo::operator=  
 [!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
```  
CMFCDesktopAlertWndInfo& operator=(  
   CMFCDesktopAlertWndInfo& src  
);  
```  
  
### Parameters  
 [in] `src`  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcdesktopalertwndinfo__m_hicon"></a>  CMFCDesktopAlertWndInfo::m_hIcon  
 A handle to the icon that is displayed.  
  
```  
HICON m_hIcon;  
```  
  
### Remarks  
  
##  <a name="cmfcdesktopalertwndinfo__m_nurlcmdid"></a>  CMFCDesktopAlertWndInfo::m_nURLCmdID  
 The command ID associated with a link on the desktop alert window.  
  
```  
UINT m_nURLCmdID;  
```  
  
### Remarks  
 The command ID is sent to the owner of the popup window when the user clicks on the link specified by [CMFCDesktopAlertWndInfo::m_strURL](#cmfcdesktopalertwndinfo__m_strurl).  
  
##  <a name="cmfcdesktopalertwndinfo__m_strtext"></a>  CMFCDesktopAlertWndInfo::m_strText  
 The text that is displayed on the desktop alert window.  
  
```  
CString m_strText;  
```  
  
### Remarks  
  
##  <a name="cmfcdesktopalertwndinfo__m_strurl"></a>  CMFCDesktopAlertWndInfo::m_strURL  
 The link that is displayed on the desktop alert window.  
  
```  
CString m_strURL;  
```  
  
### Remarks  
 When the user clicks the link, the command that has the [CMFCDesktopAlertWndInfo::m_nURLCmdID](#cmfcdesktopalertwndinfo__m_nurlcmdid) command ID will be sent to the owner of the pop-up window.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md)   
 [CMFCDesktopAlertWnd::Create](../vs140/CMFCDesktopAlertWnd-Class.md#cmfcdesktopalertwnd__create)   
 [CMFCDesktopAlertDialog Class](../vs140/CMFCDesktopAlertDialog-Class.md)