---
title: Example Code for Deleting Users on a Member Server or Windows 2000 Professional
description: This topic contain a code example that shows how to delete a user on a member server or workstation.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: '04469061-f95c-4810-99d0-03d98b70d3d3'
ms.prod: 'windows-server-dev'
ms.technology: 'active-directory-domain-services'
ms.tgt_platform: multiple
keywords: ["Active Directory examples Active Directory , deleting users on a member server or Windows 2000 Professional"]
---

# Example Code for Deleting Users on a Member Server or Windows 2000 Professional

The following Visual Basic code deletes a user on a member server or workstation.


```VB
Dim cont As IADsContainer
Dim oGroup As IADsGroup

'Example: Deleting a user on a member server or workstation
 
''''''''''''''''''''
'Parse the arguments
''''''''''''''''''''
On Error Resume Next
sComputer = InputBox("This script deletes a user from a member " _
                     & "server or workstation." _
                     & vbCrLf & vbCrLf _
                     & "Specify the computer name:")
If sComputer = "" Then
    Exit Sub
End If

sUser = InputBox("Specify the user name:")
If sUser = "" Then
    Exit Sub
End If
 
''''''''''''''''''''
'Bind to the computer
''''''''''''''''''''
Set cont = GetObject("WinNT://" & sComputer & ",computer")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
''''''''''''''''''''
'Delete the user
''''''''''''''''''''
cont.Delete "user", sUser

If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADsContainer::Delete method"
End If
 
strText = "The user " & sUser & " was deleted on computer " _
          & sComputer & "."
 
Call show_users(strText, sComputer) 
''''''''''''''''''''
'Display subroutines
''''''''''''''''''''
Sub show_users(strText, strName)
    MsgBox strText, vbInformation, "Delete user on " & strName
End Sub
```



 

 



