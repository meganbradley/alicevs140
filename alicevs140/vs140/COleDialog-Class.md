---
title: "COleDialog Class"
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
ms.assetid: b1ed0aca-3914-4b00-af34-4a4fb491aec7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDialog Class
Provides functionality common to dialog boxes for OLE.  
  
## Syntax  
  
```  
class COleDialog : public CCommonDialog  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[COleDialog::GetLastError](#coledialog__getlasterror)|Gets the error code returned by the dialog box.|  
  
## Remarks  
 The Microsoft Foundation Class Library provides several classes derived from `COleDialog`:  
  
-   [COleInsertDialog](../vs140/COleInsertDialog-Class.md)  
  
-   [COleConvertDialog](../vs140/COleConvertDialog-Class.md)  
  
-   [COleChangeIconDialog](../vs140/COleChangeIconDialog-Class.md)  
  
-   [COleLinksDialog](../vs140/COleLinksDialog-Class.md)  
  
-   [COleBusyDialog](../vs140/COleBusyDialog-Class.md)  
  
-   [COleUpdateDialog](../vs140/COleUpdateDialog-Class.md)  
  
-   [COlePasteSpecialDialog](../vs140/COlePasteSpecialDialog-Class.md)  
  
-   [COlePropertiesDialog](../vs140/COlePropertiesDialog-Class.md)  
  
-   [COleChangeSourceDialog](../vs140/COleChangeSourceDialog-Class.md)  
  
 For more information about OLE-specific dialog boxes, see the article [Dialog Boxes in OLE](../vs140/Dialog-Boxes-in-OLE.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CCommonDialog](../vs140/CCommonDialog-Class.md)  
  
 `COleDialog`  
  
## Requirements  
 **Header:** afxodlgs.h  
  
##  <a name="coledialog__getlasterror"></a>  COleDialog::GetLastError  
 Call the `GetLastError` member function to get additional error information when `DoModal` returns **IDABORT**.  
  
```  
UINT GetLastError( ) const;  
  
```  
  
### Return Value  
 The error codes returned by `GetLastError` depend on the specific dialog box displayed.  
  
### Remarks  
 See the `DoModal` member function in the derived classes for information about specific error messages.  
  
## See Also  
 [Base Class](../vs140/CCommonDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)