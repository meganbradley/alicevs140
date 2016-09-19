---
title: "VSCT XML Schema Conditional Attributes"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 754d4f32-319b-44c9-915f-f7c60e53222e
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# VSCT XML Schema Conditional Attributes
Conditional attributes may be applied to all lists and items. Logical operators and symbol expansion expressions evaluate to true or false. If true, the associated list or item is included in the resulting output.  
  
 Token expansions can be tested against other token expansions or constants. The function Defined() is used to test whether a particular name has been defined, even if it has no value.  
  
 When a Condition attribute is applied to a list, the condition is applied to every child element in the list. If a child element itself contains a Condition attribute, then its condition is combined with the parent expression by an AND operation.  
  
 The values 1, ‘1’ and ‘true’ are evaluated as true, and 0, ‘0’ and ‘false’ are evaluated as false.  
  
## Operators  
 The following operators may be used to evaluate conditional expressions.  
  
|Operator|Definition|  
|--------------|----------------|  
|(,)|Grouping|  
|!|Logical not|  
|<, >, <=, >=, ==, !=|Relational and Equality|  
|and|Boolean|  
|or|Boolean|  
  
## Examples  
  
```  
<Menu Condition="Defined(DEBUG)" …  
</Menu>  
  
<Menu Condition="%(SKU_MODE) = 'Demo'" …  
</Menu>  
  
<Menus Condition="Defined(DEBUG)">  
    <Menu …  
    </Menu>  
</Menus>  
  
<Menus Condition="Defined(DEMO_SKU)">  
    <Menus Condition="!Defined(DEBUG)">  
        <Menu …  
        </Menu>  
    </Menus>  
  
    <Menu …  
    </Menu>  
</Menus>  
  
<Menus Condition="(Defined(DEMO_SKU) or Defined(SAMPLE_SKU))   
and !Defined(DEBUG)">  
    <Menu …  
    </Menu>  
</Menus>  
```  
  
## See Also  
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)