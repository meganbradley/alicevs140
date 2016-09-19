---
title: "Help for Event Handlers in Visual Basic Code"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c92decf-844e-4ba4-82c7-f2fc0adc3002
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Help for Event Handlers in Visual Basic Code
To get Help on a particular event handler while in the code editor, put your cursor on the `Handles` clause at the back end of the event procedure, then press F1. For example, in the `Form1_Load` statement below, the correct place to put the cursor is in `MyBase.Load`:  
  
```  
Private Sub Form1_Load(ByVal sender As System.Object,   
    ByVal e As System.EventArgs) Handles MyBase.Load  
  
End Sub  
```  
  
## See Also  
 [Handling and Raising Events](assetId:///b6f65241-e0ad-4590-a99f-200ce741bb1f)   
 [Event Handlers Overview (Windows Forms)](assetId:///228112e1-1711-42ee-8ffa-ff3555bffe66)