---
title: "CButton::GetNote"
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
ms.assetid: b0db4c2d-871f-4bf6-a0ad-0a63a61d23d8
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetNote
Retrieves the note text associated with the current command link control.  
  
## Syntax  
  
```  
CString GetNote() const;  
BOOL GetNote(  
     LPTSTR lpszNote,   
     UINT* cchNote  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `lpszNote`|Pointer to a buffer, which the caller is responsible for allocating and deallocating. If the return value is `true`, the buffer contains the note text that is associated with the current command link control; otherwise, the buffer is unchanged.|  
|[in, out] `cchNote`|A pointer to an unsigned integer variable.<br /><br /> When this method is called, the variable contains the size of the buffer specified by the `lpszNote` parameter.<br /><br /> When this method returns, if the return value is `true` the variable contains the size of the note associated with the current command link control. If the return value is `false`, the variable contains the buffer size required to contain the note.|  
  
## Return Value  
 In the first overload, a [CString](../vs140/Using-CString.md) object that contains the note text associated with the current command link control.  
  
 -or-  
  
 In the second overload, `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 Use this method only with controls whose button style is `BS_COMMANDLINK` or `BS_DEFCOMMANDLINK`.  
  
 This method sends the [BCM_GETNOTE](http://msdn.microsoft.com/library/windows/desktop/bb775965) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetNote](../vs140/CButton--SetNote.md)   
 [CButton::GetNoteLength](../vs140/CButton--GetNoteLength.md)   
 [BCM_GETNOTE](http://msdn.microsoft.com/library/windows/desktop/bb775965)