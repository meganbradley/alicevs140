---
title: "COleInsertDialog::GetSelectionType"
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
ms.assetid: 71254b87-a1ff-4d7d-8360-bf00f272fc40
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleInsertDialog::GetSelectionType
Call this function to get the selection type chosen when the Insert Object dialog box was dismissed by choosing **OK**.  
  
## Syntax  
  
```  
  
UINT GetSelectionType( ) const;  
```  
  
## Return Value  
 Type of selection made.  
  
## Remarks  
 The return type values are specified by the **Selection** enumeration type declared in the `COleInsertDialog` class.  
  
 `enum Selection`  
  
 `{`  
  
 `createNewItem,`  
  
 `insertFromFile,`  
  
 `linkToFile`  
  
 `};`  
  
 Brief descriptions of these values follow:  
  
-   **COleInsertDialog::createNewItem** The Create New radio button was selected.  
  
-   **COleInsertDialog::insertFromFile** The Create From File radio button was selected and the Link check box was not checked.  
  
-   **COleInsertDialog::linkToFile** The Create From File radio button was selected and the Link check box was checked.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleInsertDialog Class](../vs140/COleInsertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleInsertDialog::DoModal](../vs140/COleInsertDialog--DoModal.md)   
 [COleInsertDialog::COleInsertDialog](../vs140/COleInsertDialog--COleInsertDialog.md)