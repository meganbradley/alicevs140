---
title: "Managed Minimun Rules rule set for managed code"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44a50c54-8dd3-42b2-8387-532a150e5a6c
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Managed Minimun Rules rule set for managed code
The Managed Minimum Rules focus on the most critical problems in your code, including potential security holes, application crashes, and other important logic and design errors. You should include this rule set in any custom rule set you create for your projects.  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1001](../vs140/CA1001--Types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1821](../vs140/CA1821--Remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA2213](../Topic/CA2213:%20Disposable%20fields%20should%20be%20disposed.md)|Disposable fields should be disposed|  
|[CA2231](../vs140/CA2231--Overload-operator-equals-on-overriding-ValueType.Equals.md)|Overload operator equals on overriding ValueType.Equals|