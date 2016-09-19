---
title: "CTreeCtrl::EndEditLabelNow"
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
ms.assetid: 43eeef8f-001c-42f4-8cc8-3130127db0e6
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::EndEditLabelNow
Concludes the edit operation on the label of a tree-view item in the current tree-view control.  
  
## Syntax  
  
```  
BOOL EndEditLabelNow(  
     BOOL fCancelWithoutSave  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `fCancelWithoutSave`|`true` to discard changes to the tree-view item before concluding the edit operation, or `false` to save changes to the tree-view item before concluding the operation.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [TVM_ENDEDITLABELNOW](http://msdn.microsoft.com/library/windows/desktop/bb773564) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows NT 3.51 and later.  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TVM_ENDEDITLABELNOW](http://msdn.microsoft.com/library/windows/desktop/bb773564)   
 [CTreeCtrl::EditLabel](../vs140/CTreeCtrl--EditLabel.md)