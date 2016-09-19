---
title: "CLinkCtrl::GetIdealSize"
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
ms.assetid: 3a025230-a9dc-4aae-962e-51a111e4aae9
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::GetIdealSize
Calculates the preferred height of the link text for the current link control, depending on the specified width of the link.  
  
## Syntax  
  
```  
int GetIdealSize(  
    int cxMaxWidth,   
    SIZE* pSize  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `cxMaxWidth`|The maximum width of the link, in pixels.|  
|[out] *`pSize`|A pointer to a Windows [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure. When this method returns, the `cy` member of the `SIZE` structure contains the ideal link text height for the link text width that is specified by `cxMaxWidth`. The `cx` member of the structure contains the link text width that is actually needed.|  
  
## Return Value  
 The preferred height of the link text, in pixels. The return value is the same as the value of the `cy` member of the `SIZE` structure.  
  
## Remarks  
 For an example of the `GetIdealSize` method, see the example in [CLinkCtrl::Create](../vs140/CLinkCtrl--Create.md).  
  
 This method sends the [LM_GETIDEALSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760718) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LM_GETIDEALSIZE](http://msdn.microsoft.com/library/windows/desktop/bb760718)   
 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106)   
 [CLinkCtrl::GetIdealHeight](../vs140/CLinkCtrl--GetIdealHeight.md)