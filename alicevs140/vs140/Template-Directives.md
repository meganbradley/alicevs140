---
title: "Template Directives"
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
ms.topic: article
ms.assetid: b6204153-813a-423c-b044-e39c352cc5af
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Template Directives
You can use the following template directives in a wizard [template file](../vs140/Template-Files.md) and the [Templates.inf file](../vs140/Templates.inf-File.md) to customize the wizard.  
  
|Directive|Description|  
|---------------|-----------------|  
|[! if ]|Begins a control structure to check for a condition.|  
|[! else ]|Part of the [! if ] control structure. Checks for another condition.|  
|[! endif ]|Ends the definition of an [! if ] control structure.|  
|[! output ]|Can be used in the following two ways:<br /><br /> -   [! output "string" ] gives you the string.<br />-   [! output SYMBOL_STRING ] gives you the value of the symbol SYMBOL_STRING.|  
|[! loop ]|Can be used in the following two ways:<br /><br /> -   [! loop = 5 ]<br />-   [! loop = *NUM_OF_PAGES* ] where *NUM_OF_PAGES* is a symbol with a numeric value.|  
|[! endloop ]|Ends a loop structure.|  
  
 The left bracket ([) followed immediately by an exclamation mark (!) indicates the beginning of a template directive. The right bracket indicates the end of a template directive. This is the required syntax:  
  
```  
[!directiveparams]  
```  
  
 A space or a non-identifier character is required only between *directive* and *params*.  
  
## Example  
  
```  
[!if SAMPLE_RADIO_OPTION1]  
You have checked the option 'Sample radio button option 1'  
[!else]  
You have checked the option 'Sample radio button option 2'  
[!endif]  
```  
  
 You can use the following operators with the above directives in a template file.  
  
```  
+  
-     
=  
!=     
==     
||     
&&    
!  
```  
  
## Example  
  
```  
[!if SYMBOL_STRING != 0]  
```  
  
## See Also  
 [Files Created for Your Wizard](../vs140/Files-Created-for-Your-Wizard.md)   
 [Custom Wizard](../vs140/Custom-Wizard.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)