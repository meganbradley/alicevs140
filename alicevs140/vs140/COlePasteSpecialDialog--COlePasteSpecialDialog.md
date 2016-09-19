---
title: "COlePasteSpecialDialog::COlePasteSpecialDialog"
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
ms.assetid: 7a442726-9060-4518-ae89-c1d078efa3f6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::COlePasteSpecialDialog
Constructs a `COlePasteSpecialDialog` object.  
  
## Syntax  
  
```  
  
      COlePasteSpecialDialog(  
   DWORD dwFlags = PSF_SELECTPASTE,  
   COleDataObject* pDataObject = NULL,  
   CWnd* pParentWnd = NULL   
);  
```  
  
#### Parameters  
 `dwFlags`  
 Creation flag, contains any number of the following flags combined using the bitwise-OR operator:  
  
-   `PSF_SELECTPASTE` Specifies that the Paste radio button will be checked initially when the dialog box is called. Cannot be used in combination with `PSF_SELECTPASTELINK`. This is the default.  
  
-   `PSF_SELECTPASTELINK` Specifies that the Paste Link radio button will be checked initially when the dialog box is called. Cannot be used in combination with `PSF_SELECTPASTE`.  
  
-   `PSF_CHECKDISPLAYASICON` Specifies that the Display As Icon check box will be checked initially when the dialog box is called.  
  
-   `PSF_SHOWHELP` Specifies that the Help button will be displayed when the dialog box is called.  
  
 `pDataObject`  
 Points to the [COleDataObject](../vs140/COleDataObject-Class.md) for pasting. If this value is **NULL**, it gets the `COleDataObject` from the Clipboard.  
  
 `pParentWnd`  
 Points to the parent or owner window object (of type `CWnd`) to which the dialog object belongs. If it is **NULL**, the parent window of the dialog box is set to the main application window.  
  
## Remarks  
 This function only constructs a `COlePasteSpecialDialog` object. To display the dialog box, call the [DoModal](../vs140/COlePasteSpecialDialog--DoModal.md) function.  
  
 For more information, see the [OLEUIPASTEFLAG](http://msdn.microsoft.com/library/windows/desktop/ms682172) enumerated type in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [COlePasteSpecialDialog::DoModal](../vs140/COlePasteSpecialDialog--DoModal.md)