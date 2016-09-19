---
title: "CA2233: Operations should not overflow"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a2b06ba-6d1b-4666-9eaf-e053ef47ffaa
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2233: Operations should not overflow
|||  
|-|-|  
|TypeName|OperationsShouldNotOverflow|  
|CheckId|CA2233|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A method performs an arithmetic operation and does not validate the operands beforehand to prevent overflow.  
  
## Rule Description  
 Arithmetic operations should not be performed without first validating the operands to make sure that the result of the operation is not outside the range of possible values for the data types involved. Depending on the execution context and the data types involved, arithmetic overflow can result in either a <xref:System.OverflowException?qualifyHint=True> or the most significant bits of the result discarded.  
  
## How to Fix Violations  
 To fix a violation of this rule, validate the operands before you perform the operation.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule if the possible values of the operands will never cause the arithmetic operation to overflow.  
  
## Example of a Violation  
  
### Description  
 A method in the following example manipulates an integer that violates this rule. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] requires the **Remove** integer overflow option to be disabled for this to fire.  
  
### Code  
 [!CODE [FxCop.Usage.OperationOverflow#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.OperationOverflow#1)]  
  
### Comments  
 If the method in this example is passed <xref:System.Int32.MinValue?qualifyHint=True>, the operation would underflow. This causes the most significant bit of the result to be discarded. The following code shows how this occurs.  
  
 [C#]  
  
```  
public static void Main()  
{  
    int value = int.MinValue;    // int.MinValue is -2147483648   
    value = Calculator.Decrement(value);   
    Console.WriteLine(value);  
}  
```  
  
 [VB]  
  
```  
Public Shared Sub Main()       
    Dim value = Integer.MinValue    ' Integer.MinValue is -2147483648   
    value = Calculator.Decrement(value)   
    Console.WriteLine(value)   
End Sub  
```  
  
### Output  
  
```  
2147483647  
```  
  
## Fix with Input Parameter Validation  
  
### Description  
 The following example fixes the previous violation by validating the value of input.  
  
### Code  
 [!CODE [FxCop.Usage.OperationOverflowFixed#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.OperationOverflowFixed#1)]  
  
## Fix with a Checked Block  
  
### Description  
 The following example fixes the previous violation by wrapping the operation in a checked block. If the operation causes an overflow, a <xref:System.OverflowException?qualifyHint=True> will be thrown.  
  
 Note that checked blocks are not supported in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)].  
  
### Code  
 [!CODE [FxCop.Usage.OperationOverflowChecked#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Usage.OperationOverflowChecked#1)]  
  
## Turn on Checked Arithmetic Overflow/Underflow  
 If you turn on checked arithmetic overflow/underflow in C#, it is equivalent to wrapping every integer operation in a checked block.  
  
 **To turn on checked arithmetic overflow/underflow in C#**  
  
1.  In **Solution Explorer**, right-click your project and choose **Properties**.  
  
2.  Select the **Build** tab and click **Advanced**.  
  
3.  Select **Check for arithmetic overflow/underflow** and click **OK**.  
  
## See Also  
 <xref:System.OverflowException?qualifyHint=True>   
 [C# Operators - Arithmetic Overflow](../Topic/C%23%20Operators.md)   
 [C# Checked and Unchecked](../vs140/Checked-and-Unchecked--C#-Reference-.md)