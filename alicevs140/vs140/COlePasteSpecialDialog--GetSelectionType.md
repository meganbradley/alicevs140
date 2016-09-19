---
title: "COlePasteSpecialDialog::GetSelectionType"
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
ms.assetid: 944ef6cb-e222-40bf-a3d6-7d45751761ac
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::GetSelectionType
Determines the type of selection the user made.  
  
## Syntax  
  
```  
  
UINT GetSelectionType( ) const;  
```  
  
## Return Value  
 Returns type of selection made.  
  
## Remarks  
 The return type values are specified by the **Selection** enumeration type declared in the `COlePasteSpecialDialog` class.  
  
 `enum Selection`  
  
 `{`  
  
 `pasteLink,`  
  
 `pasteNormal,`  
  
 `pasteOther,`  
  
 `pasteStatic`  
  
 `};`  
  
 Brief desccriptions of these values follow:  
  
-   **COlePasteSpecialDialog::pasteLink** The Paste Link radio button was checked and the chosen format was a standard OLE format.  
  
-   **COlePasteSpecialDialog::pasteNormal** The Paste radio button was checked and the chosen format was a standard OLE format.  
  
-   **COlePasteSpecialDialog::pasteOther** The selected format is not a standard OLE format.  
  
-   **COlePasteSpecialDialog::pasteStatic** The chosen format was a metafile.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePasteSpecialDialog::DoModal](../vs140/COlePasteSpecialDialog--DoModal.md)