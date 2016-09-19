---
title: "CFolderPickerDialog Class"
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
ms.assetid: 8db01684-dd1d-4e9c-989e-07a2318a8156
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFolderPickerDialog Class
CFolderPickerDialog class implements CFileDialog in the folder picker mode.  
  
## Syntax  
  
```  
class CFolderPickerDialog : public CFileDialog;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CFolderPickerDialog::~CFolderPickerDialog](#cfolderpickerdialog__~cfolderpickerdialog)|Destructor.|  
|[CFolderPickerDialog::CFolderPickerDialog](#cfolderpickerdialog__cfolderpickerdialog)|Constructor.|  
  
## Remarks  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CCommonDialog](../vs140/CCommonDialog-Class.md)  
  
 [CFileDialog](../vs140/CFileDialog-Class.md)  
  
 `CFolderPickerDialog`  
  
## Requirements  
 **Header:** afxdlgs.h  
  
##  <a name="cfolderpickerdialog__cfolderpickerdialog"></a>  CFolderPickerDialog::CFolderPickerDialog  
 Constructor.  
  
```  
explicit CFolderPickerDialog(  
   LPCTSTR lpszFolder = NULL,  
   DWORD dwFlags = 0,  
   CWnd* pParentWnd = NULL,  
   DWORD dwSize = 0  
);  
```  
  
### Parameters  
 `lpszFolder`  
 Initial folder.  
  
 `dwFlags`  
 A combination of one or more flags that allow you to customize the dialog box.  
  
 `pParentWnd`  
 A pointer to the dialog box object's parent or owner window.  
  
 `dwSize`  
 The size of the OPENFILENAME structure.  
  
### Remarks  
  
##  <a name="cfolderpickerdialog___dtorcfolderpickerdialog"></a>  CFolderPickerDialog::~CFolderPickerDialog  
 Destructor.  
  
```  
virtual ~CFolderPickerDialog();  
```  
  
### Remarks  
  
## See Also  
 [Classes](../vs140/MFC-Classes.md)