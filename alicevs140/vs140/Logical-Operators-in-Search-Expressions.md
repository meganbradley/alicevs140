---
title: "Logical Operators in Search Expressions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0c38ae7d-3e20-4d47-a020-9677cd285916
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Logical Operators in Search Expressions
By using logical operators, you can refine your search for content by creating more complicated search expressions from simpler ones. As the following table shows, logical operators specify how multiple search terms should be combined in a search query.  
  
> [!IMPORTANT]
>  You must enter logical operators in all capital letters for the search engine to recognize them.  
  
|To search for|Use|Example|Result|  
|-------------------|---------|-------------|------------|  
|Both terms in the same topic|AND|dib AND palette|Topics that contain both "dib" and "palette".|  
|Either term in a topic|OR|raster OR vector|Topics that contain either "raster" or "vector".|  
|First term without the second term in the same topic|NOT|"operating system" NOT DOS|Topics that contain "operating system" but not "DOS".|  
|Both terms, close together in a topic|NEAR|user NEAR kernel|Topics that contain "user" within close proximity of "kernel".|  
  
## See Also  
 [Full Text Searches](../vs140/Full-Text-Search-Tips.md)   
 [Techniques for Locating Help](../vs140/Locate-Information.md)