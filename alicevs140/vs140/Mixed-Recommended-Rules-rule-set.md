---
title: "Mixed Recommended Rules rule set"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c3186b5b-0149-4a75-826e-e3539e4e703f
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mixed Recommended Rules rule set
The Microsoft Mixed Recommended Rules focus on the most common and critical problems in your C++ projects that support the Common Language Runtime, including potential security holes, application crashes, and other important logic and design errors. You should include this rule set in any custom rule set you create for your C++ projects that support the Common Language Runtime. This ruleset is designed to be configured with the Visual Studio Professional edition and higher.  
  
|Rule|Description|  
|----------|-----------------|  
|[C6001](../vs140/C6001.md)|Using Uninitialized Memory|  
|[C6011](../vs140/C6011.md)|Dereferencing Null Pointer|  
|[C6029](../vs140/C6029.md)|Use Of Unchecked Value|  
|[C6031](../vs140/C6031.md)|Return Value Ignored|  
|[C6053](../vs140/C6053.md)|Zero Termination From Call|  
|[C6054](../vs140/C6054.md)|Zero Termination Missing|  
|[C6059](../vs140/C6059.md)|Bad Concatenation|  
|[C6063](../vs140/C6063.md)|Missing String Argument To Format Function|  
|[C6064](../vs140/C6064.md)|Missing Integer Argument To Format Function|  
|[C6066](../vs140/C6066.md)|Missing Pointer Argument To Format Function|  
|[C6067](../vs140/C6067.md)|Missing String Pointer Argument To Format Function|  
|[C6101](../vs140/C6101.md)|Returning uninitialized memory|  
|[C6200](../vs140/C6200.md)|Index Exceeds Buffer Maximum|  
|[C6201](../vs140/C6201.md)|Index Exceeds Stack Buffer Maximum|  
|[C6214](../vs140/C6214.md)|Invalid Cast HRESULT To BOOL|  
|[C6215](../vs140/C6215.md)|Invalid Cast BOOL To HRESULT|  
|[C6216](../vs140/C6216.md)|Invalid Compiler-Inserted Cast BOOL To HRESULT|  
|[C6217](../vs140/C6217.md)|Invalid HRESULT Test With NOT|  
|[C6220](../vs140/C6220.md)|Invalid HRESULT Compare To -1|  
|[C6226](../vs140/C6226.md)|Invalid HRESULT Assignment To -1|  
|[C6230](../vs140/C6230.md)|Invalid HRESULT Use As Boolean|  
|[C6235](../vs140/C6235.md)|Non-Zero Constant With Logical-Or|  
|[C6236](../vs140/C6236.md)|Logical-Or With Non-Zero Constant|  
|[C6237](../vs140/C6237.md)|Zero With Logical-And Loses Side Effects|  
|[C6242](../vs140/C6242.md)|Local Unwind Forced|  
|[C6248](../vs140/C6248.md)|Creating Null DACL|  
|[C6250](../vs140/C6250.md)|Unreleased Address Descriptors|  
|[C6255](../vs140/C6255.md)|Unprotected Use Of Alloca|  
|[C6258](../vs140/C6258.md)|Using Terminate Thread|  
|[C6259](../vs140/C6259.md)|Dead Code In Bitwise-Or Limited Switch|  
|[C6260](../vs140/C6260.md)|Use Of Byte Arithmetic|  
|[C6262](../vs140/C6262.md)|Excessive Stack Usage|  
|[C6263](../vs140/C6263.md)|Using Alloca In Loop|  
|[C6268](../vs140/C6268.md)|Missing Parentheses In Cast|  
|[C6269](../vs140/C6269.md)|Pointer Dereference Ignored|  
|[C6270](../vs140/C6270.md)|Missing Float Argument To Format Function|  
|[C6271](../vs140/C6271.md)|Extra Argument To Format Function|  
|[C6272](../vs140/C6272.md)|Non-Float Argument To Format Function|  
|[C6273](../vs140/C6273.md)|Non-Integer Argumen To Format Function|  
|[C6274](../vs140/C6274.md)|Non-Character Argument To Format Function|  
|[C6276](../vs140/C6276.md)|Invalid String Cast|  
|[C6277](../vs140/C6277.md)|Invalid CreateProcess Call|  
|[C6278](../vs140/C6278.md)|Array-New Scalar-Delete Mismatch|  
|[C6279](../vs140/C6279.md)|Scalar-New Array-Delete Mismatch|  
|[C6280](../vs140/C6280.md)|Memory Allocation-Deallocation Mismatch|  
|[C6281](../vs140/C6281.md)|Bitwise Relation Precedence|  
|[C6282](../vs140/C6282.md)|Assignment Replaces Test|  
|[C6283](../vs140/C6283.md)|Primitive Array-New Scalar-Delete Mismatch|  
|[C6284](../vs140/C6284.md)|Invalid Object Argument To Format Function|  
|[C6285](../vs140/C6285.md)|Logical-Or Of Constants|  
|[C6286](../vs140/C6286.md)|Non-Zero Logical-Or Losing Side Effects|  
|[C6287](../vs140/C6287.md)|Redundant Test|  
|[C6288](../vs140/C6288.md)|Mutual Inclusion Over Logical-And Is False|  
|[C6289](../vs140/C6289.md)|Mutual Exclusion Over Logical-Or Is True|  
|[C6290](../vs140/C6290.md)|Logical-Not Bitwise-And Precedence|  
|[C6291](../vs140/C6291.md)|Logical-Not Bitwise-Or Precedence|  
|[C6292](../vs140/C6292.md)|Loop Counts Up From Maximum|  
|[C6293](../vs140/C6293.md)|Loop Counts Down From Minimum|  
|[C6294](../vs140/C6294.md)|Loop Body Never Executed|  
|[C6295](../vs140/C6295.md)|Infinite Loop|  
|[C6296](../vs140/C6296.md)|Loop Only Executed Once|  
|[C6297](../vs140/C6297.md)|Result Of Shift Cast To Larger Size|  
|[C6299](../vs140/C6299.md)|Bitfield To Boolean Comparison|  
|[C6302](../vs140/C6302.md)|Invalid Character String Argument To Format Function|  
|[C6303](../vs140/C6303.md)|Invalid Wide Character String Argument To Format Function|  
|[C6305](../vs140/C6305.md)|Mismatched Size And Count Use|  
|[C6306](../vs140/C6306.md)|Incorrect Variable Argument Function Call|  
|[C6308](../vs140/C6308.md)|Realloc Leak|  
|[C6310](../vs140/C6310.md)|Illegal Exception Filter Constant|  
|[C6312](../vs140/C6312.md)|Exception Continue Execution Loop|  
|[C6314](../vs140/C6314.md)|Bitwise-Or Precedence|  
|[C6317](../vs140/C6317.md)|Not Not Complement|  
|[C6318](../vs140/C6318.md)|Exception Continue Search|  
|[C6319](../vs140/C6319.md)|Ignored By Comma|  
|[C6324](../vs140/C6324.md)|String Copy Instead Of String Compare|  
|[C6328](../vs140/C6328.md)|Potential Argument Type Mismatch|  
|[C6331](../vs140/C6331.md)|VirtualFree Invalid Flags|  
|[C6332](../vs140/C6332.md)|VirtualFree Invalid Parameter|  
|[C6333](../vs140/C6333.md)|VirtualFree Invalid Size|  
|[C6335](../vs140/C6335.md)|Leaking Process Handle|  
|[C6381](../vs140/C6381.md)|Shutdown Information Missing|  
|[C6383](../vs140/C6383.md)|Element-Count Byte-Count Buffer Overrun|  
|[C6384](../vs140/C6384.md)|Pointer Size Division|  
|[C6385](../vs140/C6385.md)|Read Overrun|  
|[C6386](../vs140/C6386.md)|Write Overrun|  
|[C6387](../vs140/C6387.md)|Invalid Parameter Value|  
|[C6388](../vs140/C6388.md)|Invalid Parameter Value|  
|[C6500](../vs140/C6500.md)|Invalid Attribute Property|  
|[C6501](../vs140/C6501.md)|Conflicting Attribute Property Values|  
|[C6503](../vs140/C6503.md)|References Cannot Be Null|  
|[C6504](../vs140/C6504.md)|Null On Non-Pointer|  
|[C6505](../vs140/C6505.md)|MustCheck On Void|  
|[C6506](../vs140/C6506.md)|Buffer Size On Non-Pointer Or Array|  
|[C6507](assetId:///18f88cd1-d035-4403-a6a4-12dd0affcf21)|Null Mismatch At Dereference Zero|  
|[C6508](../vs140/C6508.md)|Write Access On Constant|  
|[C6509](../vs140/C6509.md)|Return Used On Precondition|  
|[C6510](../vs140/C6510.md)|Null Terminated On Non-Pointer|  
|[C6511](../vs140/C6511.md)|MustCheck Must Be Yes Or No|  
|[C6513](../vs140/C6513.md)|Element Size Without Buffer Size|  
|[C6514](../vs140/C6514.md)|Buffer Size Exceeds Array Size|  
|[C6515](../vs140/C6515.md)|Buffer Size On Non-Pointer|  
|[C6516](../vs140/C6516.md)|No Properties On Attribute|  
|[C6517](../vs140/C6517.md)|Valid Size On Non-Readable Buffer|  
|[C6518](../vs140/C6518.md)|Writable Size On Non-Writable Buffer|  
|[C6519](assetId:///2b6326b0-0539-4d26-8fb1-720114933232)|Invalid annotation: value of the 'NeedsRelease' property must be Yes or No|  
|[C6521](assetId:///e98d0ae3-6f13-47b2-9a15-15d4055af9ef)|Invalid Size String Dereference|  
|[C6522](../vs140/C6522.md)|Invalid Size String Type|  
|[C6523](assetId:///11397a31-b224-46b0-afb7-d49ca576a3bb)|Invalid Size String Parameter|  
|[C6525](../vs140/C6525.md)|Invalid Size String Unreachable Location|  
|[C6526](assetId:///59c590c7-0098-4166-a1ac-87f324596002)|Invalid Size String Buffer Type|  
|[C6527](../vs140/C6527.md)|Invalid annotation: 'NeedsRelease' property may not be used on values of void type|  
|[C6530](../vs140/C6530.md)|Unrecognized Format String Style|  
|[C6540](../vs140/C6540.md)|The use of attribute annotations on this function will invalidate all of its existing __declspec annotations|  
|[C6551](../vs140/C6551.md)|Invalid size specification: expression not parsable|  
|[C6552](../vs140/C6552.md)|Invalid Deref= or Notref=: expression not parsable|  
|[C6701](../vs140/C6701.md)|The value is not a valid Yes/No/Maybe value|  
|[C6702](../vs140/C6702.md)|The value is not a string value|  
|[C6703](../vs140/C6703.md)|The value is not a number|  
|[C6704](../vs140/C6704.md)|Unexpected Annotation Expression Error|  
|[C6705](../vs140/C6705.md)|Expected number of arguments for annotation does not match actual number of arguments for annotation|  
|[C6706](../vs140/C6706.md)|Unexpected Annotation Error for annotation|  
|[C6995](../vs140/C6995.md)|Failed to save XML Log file|  
|[C26100](../vs140/C26100.md)|Race condition|  
|[C26101](../vs140/C26101.md)|Failing to use interlocked operation properly|  
|[C26110](../vs140/C26110.md)|Caller failing to hold lock|  
|[C26111](../vs140/C26111.md)|Caller failing to release lock|  
|[C26112](../vs140/C26112.md)|Caller cannot hold any lock|  
|[C26115](../vs140/C26115.md)|Failing to release lock|  
|[C26116](../vs140/C26116.md)|Failing to acquire or to hold lock|  
|[C26117](../vs140/C26117.md)|Releasing unheld lock|  
|[C26140](../vs140/C26140.md)|Concurrency SAL annotation error|  
|[C28020](../vs140/C28020.md)|The expression is not true at this call|  
|[C28021](../vs140/C28021.md)|The parameter being annotated must be a pointer|  
|[C28022](../vs140/C28022.md)|The function class(es) on this function do not match the function class(es) on the typedef used to define it.|  
|[C28023](../vs140/C28023.md)|The function being assigned or passed should have a _Function_class\_ annotation for at least one of the class(es)|  
|[C28024](../vs140/C28024.md)|The function pointer being assigned to is annotated with the function class, which is not contained in the function class(es) list.|  
|[C28039](../vs140/C28039.md)|The type of actual parameter should exactly match the type|  
|[C28112](../vs140/C28112.md)|A variable which is accessed via an Interlocked function must always be accessed via an Interlocked function.|  
|[C28113](../vs140/C28113.md)|Accessing a local variable via an Interlocked function|  
|[C28125](../vs140/C28125.md)|The function must be called from within a try/except block|  
|[C28137](../vs140/C28137.md)|The variable argument should instead be a (literal) constant|  
|[C28138](../vs140/C28138.md)|The constant argument should instead be variable|  
|[C28159](../vs140/C28159.md)|Consider using another function instead.|  
|[C28160](../vs140/C28160.md)|Error annotation|  
|[C28163](../vs140/C28163.md)|The function should never be called from within a try/except block|  
|[C28164](../vs140/C28164.md)|The argument is being passed to a function that expects a pointer to an object (not a pointer to a pointer)|  
|[C28182](../vs140/C28182.md)|Dereferencing NULL pointer. The pointer contains the same NULL value as another pointer did.|  
|[C28183](../vs140/C28183.md)|The argument could be one value, and is a copy of the value found in the pointer|  
|[C28193](../vs140/C28193.md)|The variable holds a value that must be examined|  
|[C28196](../vs140/C28196.md)|The requirement is not satisfied. (The expression does not evaluate to true.)|  
|[C28202](../vs140/C28202.md)|Illegal reference to non-static member|  
|[C28203](../vs140/C28203.md)|Ambiguous reference to class member.|  
|[C28205](../vs140/C28205.md)|_Success\_ or _On_failure\_ used in an illegal context|  
|[C28206](../vs140/C28206.md)|Left operand points to a struct, use '->'|  
|[C28207](../vs140/C28207.md)|Left operand is a struct, use '.'|  
|[C28209](../vs140/C28209.md)|The declaration for symbol has a conflicting declaration|  
|[C28210](../vs140/C28210.md)|Annotations for the __on_failure context must not be in explicit pre context|  
|[C28211](../vs140/C28211.md)|Static context name expected for SAL_context|  
|[C28212](../vs140/C28212.md)|Pointer expression expected for annotation|  
|[C28213](../vs140/C28213.md)|The _Use_decl_annotations\_ annotation must be used to reference, without modification, a prior declaration.|  
|[C28214](../vs140/C28214.md)|Attribute parameter names must be p1...p9|  
|[C28215](../vs140/C28215.md)|The typefix cannot be applied to a parameter that already has a typefix|  
|[C28216](../vs140/C28216.md)|The checkReturn annotation only applies to postconditions for the specific function parameter.|  
|[C28217](../vs140/C28217.md)|For function, the number of parameters to annotation does not match that found at file|  
|[C28218](../vs140/C28218.md)|For function paramteer, the annotation's parameter does not match that found at file|  
|[C28219](../vs140/C28219.md)|Member of enumeration expected for annotation the parameter in the annotation|  
|[C28220](../vs140/C28220.md)|Integer expression expected for annotation the parameter in the annotation|  
|[C28221](../vs140/C28221.md)|String expression expected for the parameter in the annotation|  
|[C28222](../vs140/C28222.md)|__yes, \__no, or \__maybe expected for annotation|  
|[C28223](../vs140/C28223.md)|Did not find expected Token/identifier for annotation, parameter|  
|[C28224](../vs140/C28224.md)|Annotation requires parameters|  
|[C28225](../vs140/C28225.md)|Did not find the correct number of required parameters in annotation|  
|[C28226](../vs140/C28226.md)|Annotation cannot also be a PrimOp (in current declaration)|  
|[C28227](../vs140/C28227.md)|Annotation cannot also be a PrimOp (see prior declaration)|  
|[C28228](../vs140/C28228.md)|Annotation parameter: cannot use type in annotations|  
|[C28229](../vs140/C28229.md)|Annotation does not support parameters|  
|[C28230](../vs140/C28230.md)|The type of parameter has no member.|  
|[C28231](../vs140/C28231.md)|Annotation is only valid on array|  
|[C28232](../vs140/C28232.md)|pre, post, or deref not applied to any annotation|  
|[C28233](../vs140/C28233.md)|pre, post, or deref applied to a block|  
|[C28234](../vs140/C28234.md)|__at expression does not apply to current function|  
|[C28235](../vs140/C28235.md)|The function cannot stand alone as an annotation|  
|[C28236](../vs140/C28236.md)|The annotation cannot be used in an expression|  
|[C28237](../vs140/C28237.md)|The annotation on parameter is no longer supported|  
|[C28238](../vs140/C28238.md)|The annotation on parameter has more than one of value, stringValue, and longValue. Use paramn=xxx|  
|[C28239](../vs140/C28239.md)|The annotation on parameter has both value, stringValue, or longValue; and paramn=xxx. Use only paramn=xxx|  
|[C28240](../vs140/C28240.md)|The annotation on parameter has param2 but no param1|  
|[C28241](../vs140/C28241.md)|The annotation for function on parameter is not recognized|  
|[C28243](../vs140/C28243.md)|The annotation for function on parameter requires more dereferences than the actual type annotated allows|  
|[C28244](../vs140/C28244.md)|The annotation for function has an unparseable parameter/external annotation|  
|[C28245](../vs140/C28245.md)|The annotation for function annotates 'this' on a non-member-function|  
|[C28246](../vs140/C28246.md)|The parameter annotation for function does not match the type of the parameter|  
|[C28250](../vs140/C28250.md)|Inconsistent annotation for function: the prior instance has an error.|  
|[C28251](../vs140/C28251.md)|Inconsistent annotation for function: this instance has an error.|  
|[C28252](../vs140/C28252.md)|Inconsistent annotation for function: parameter has another annotations on this instance.|  
|[C28253](../vs140/C28253.md)|Inconsistent annotation for function: parameter has another annotations on this instance.|  
|[C28254](../vs140/C28254.md)|dynamic_cast<>() is not supported in annotations|  
|[C28262](../vs140/C28262.md)|A syntax error in the annotation was found in function, for annotation|  
|[C28263](../vs140/C28263.md)|A syntax error in a conditional annotation was found for Intrinsic annotation|  
|[C28264](assetId:///bf6ea983-a06e-4752-a042-747a7dbf338c)|Result lists values must be constants.|  
|[C28267](../vs140/C28267.md)|A syntax error in the annotations was found annotation in the function.|  
|[C28272](../vs140/C28272.md)|The annotation for function, parameter when examining is inconsistent with the function declaration|  
|[C28273](../vs140/C28273.md)|For function, the clues are inconsistent with the function declaration|  
|[C28275](../vs140/C28275.md)|The parameter to _Macro_value\_ is null|  
|[C28279](../vs140/C28279.md)|For symbol, a 'begin' was found without a matching 'end'|  
|[C28280](../vs140/C28280.md)|For symbol, an 'end' was found without a matching 'begin'|  
|[C28282](../vs140/C28282.md)|Format Strings must be in preconditions|  
|[C28285](../vs140/C28285.md)|For function, syntax error in parameter|  
|[C28286](../vs140/C28286.md)|For function, syntax error near the end|  
|[C28287](../vs140/C28287.md)|For function, syntax Error in _At\_() annotation (unrecognized parameter name)|  
|[C28288](../vs140/C28288.md)|For function, syntax Error in _At\_() annotation (invalid parameter name)|  
|[C28289](../vs140/C28289.md)|For function: ReadableTo or WritableTo did not have a limit-spec as a parameter|  
|[C28290](../vs140/C28290.md)|the annotation for function contains more Externals than the actual number of parameters|  
|[C28291](../vs140/C28291.md)|post null/notnull at deref level 0 is meaningless for function.|  
|[C28300](../vs140/C28300.md)|Expression operands of incompatible types for operator|  
|[C28301](../vs140/C28301.md)|No annotations for first declaration of function.|  
|[C28302](../vs140/C28302.md)|An extra _Deref\_ operator was found on annotation.|  
|[C28303](../vs140/C28303.md)|An ambiguous _Deref\_ operator was found on annotation.|  
|[C28304](../vs140/C28304.md)|An improperly placed _Notref\_ operator was found applied to token.|  
|[C28305](../vs140/C28305.md)|An error while parsing a token was discovered.|  
|[C28306](../vs140/C28306.md)|The annotation on parameter is obsolescent|  
|[C28307](../vs140/C28307.md)|The annotation on parameter is obsolescent|  
|[C28350](../vs140/C28350.md)|The annotation describes a situation that is not conditionally applicable.|  
|[C28351](../vs140/C28351.md)|The annotation describes where a dynamic value (a variable) cannot be used in the condition.|  
|[CA1001](../vs140/CA1001--Types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1009](../Topic/CA1009:%20Declare%20event%20handlers%20correctly.md)|Declare event handlers correctly|  
|[CA1016](../Topic/CA1016:%20Mark%20assemblies%20with%20AssemblyVersionAttribute.md)|Mark assemblies with AssemblyVersionAttribute|  
|[CA1033](../vs140/CA1033--Interface-methods-should-be-callable-by-child-types.md)|Interface methods should be callable by child types|  
|[CA1049](../Topic/CA1049:%20Types%20that%20own%20native%20resources%20should%20be%20disposable.md)|Types that own native resources should be disposable|  
|[CA1060](../vs140/CA1060--Move-P-Invokes-to-NativeMethods-class.md)|Move P/Invokes to NativeMethods class|  
|[CA1061](../vs140/CA1061--Do-not-hide-base-class-methods.md)|Do not hide base class methods|  
|[CA1063](../vs140/CA1063--Implement-IDisposable-correctly.md)|Implement IDisposable correctly|  
|[CA1065](../Topic/CA1065:%20Do%20not%20raise%20exceptions%20in%20unexpected%20locations.md)|Do not raise exceptions in unexpected locations|  
|[CA1301](../Topic/CA1301:%20Avoid%20duplicate%20accelerators.md)|Avoid duplicate accelerators|  
|[CA1400](../Topic/CA1400:%20P-Invoke%20entry%20points%20should%20exist.md)|P/Invoke entry points should exist|  
|[CA1401](../vs140/CA1401--P-Invokes-should-not-be-visible.md)|P/Invokes should not be visible|  
|[CA1403](../Topic/CA1403:%20Auto%20layout%20types%20should%20not%20be%20COM%20visible.md)|Auto layout types should not be COM visible|  
|[CA1404](../Topic/CA1404:%20Call%20GetLastError%20immediately%20after%20P-Invoke.md)|Call GetLastError immediately after P/Invoke|  
|[CA1405](../Topic/CA1405:%20COM%20visible%20type%20base%20types%20should%20be%20COM%20visible.md)|COM visible type base types should be COM visible|  
|[CA1410](../vs140/CA1410--COM-registration-methods-should-be-matched.md)|COM registration methods should be matched|  
|[CA1415](../vs140/CA1415--Declare-P-Invokes-correctly.md)|Declare P/Invokes correctly|  
|[CA1821](../vs140/CA1821--Remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA1900](../vs140/CA1900--Value-type-fields-should-be-portable.md)|Value type fields should be portable|  
|[CA1901](../vs140/CA1901--P-Invoke-declarations-should-be-portable.md)|P/Invoke declarations should be portable|  
|[CA2002](../Topic/CA2002:%20Do%20not%20lock%20on%20objects%20with%20weak%20identity.md)|Do not lock on objects with weak identity|  
|[CA2100](../vs140/CA2100--Review-SQL-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2101](../vs140/CA2101--Specify-marshaling-for-P-Invoke-string-arguments.md)|Specify marshaling for P/Invoke string arguments|  
|[CA2108](../vs140/CA2108--Review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2111](../Topic/CA2111:%20Pointers%20should%20not%20be%20visible.md)|Pointers should not be visible|  
|[CA2112](../vs140/CA2112--Secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../vs140/CA2114--Method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2116](../vs140/CA2116--APTCA-methods-should-only-call-APTCA-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../Topic/CA2117:%20APTCA%20types%20should%20only%20extend%20APTCA%20base%20types.md)|APTCA types should only extend APTCA base types|  
|[CA2122](../vs140/CA2122--Do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../vs140/CA2123--Override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../vs140/CA2124--Wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../vs140/CA2126--Type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2131](../vs140/CA2131--Security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../Topic/CA2132:%20Default%20constructors%20must%20be%20at%20least%20as%20critical%20as%20base%20type%20default%20constructors.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../vs140/CA2133--Delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../vs140/CA2134--Methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2137](../Topic/CA2137:%20Transparent%20methods%20must%20contain%20only%20verifiable%20IL.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../Topic/CA2138:%20Transparent%20methods%20must%20not%20call%20methods%20with%20the%20SuppressUnmanagedCodeSecurity%20attribute.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2140](../vs140/CA2140--Transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../Topic/CA2141:Transparent%20methods%20must%20not%20satisfy%20LinkDemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2146](../Topic/CA2146:%20Types%20must%20be%20at%20least%20as%20critical%20as%20their%20base%20types%20and%20interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../vs140/CA2147--Transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../Topic/CA2149:%20Transparent%20methods%20must%20not%20call%20into%20native%20code.md)|Transparent methods must not call into native code|  
|[CA2200](../vs140/CA2200--Rethrow-to-preserve-stack-details.md)|Rethrow to preserve stack details|  
|[CA2202](../vs140/CA2202--Do-not-dispose-objects-multiple-times.md)|Do not dispose objects multiple times|  
|[CA2207](../vs140/CA2207--Initialize-value-type-static-fields-inline.md)|Initialize value type static fields inline|  
|[CA2212](../vs140/CA2212--Do-not-mark-serviced-components-with-WebMethod.md)|Do not mark serviced components with WebMethod|  
|[CA2213](../Topic/CA2213:%20Disposable%20fields%20should%20be%20disposed.md)|Disposable fields should be disposed|  
|[CA2214](../vs140/CA2214--Do-not-call-overridable-methods-in-constructors.md)|Do not call overridable methods in constructors|  
|[CA2216](../Topic/CA2216:%20Disposable%20types%20should%20declare%20finalizer.md)|Disposable types should declare finalizer|  
|[CA2220](../Topic/CA2220:%20Finalizers%20should%20call%20base%20class%20finalizer.md)|Finalizers should call base class finalizer|  
|[CA2229](../Topic/CA2229:%20Implement%20serialization%20constructors.md)|Implement serialization constructors|  
|[CA2231](../vs140/CA2231--Overload-operator-equals-on-overriding-ValueType.Equals.md)|Overload operator equals on overriding ValueType.Equals|  
|[CA2232](../Topic/CA2232:%20Mark%20Windows%20Forms%20entry%20points%20with%20STAThread.md)|Mark Windows Forms entry points with STAThread|  
|[CA2235](../Topic/CA2235:%20Mark%20all%20non-serializable%20fields.md)|Mark all non-serializable fields|  
|[CA2236](../Topic/CA2236:%20Call%20base%20class%20methods%20on%20ISerializable%20types.md)|Call base class methods on ISerializable types|  
|[CA2237](../vs140/CA2237--Mark-ISerializable-types-with-SerializableAttribute.md)|Mark ISerializable types with SerializableAttribute|  
|[CA2238](../Topic/CA2238:%20Implement%20serialization%20methods%20correctly.md)|Implement serialization methods correctly|  
|[CA2240](../Topic/CA2240:%20Implement%20ISerializable%20correctly.md)|Implement ISerializable correctly|  
|[CA2241](../Topic/CA2241:%20Provide%20correct%20arguments%20to%20formatting%20methods.md)|Provide correct arguments to formatting methods|  
|[CA2242](../Topic/CA2242:%20Test%20for%20NaN%20correctly.md)|Test for NaN correctly|