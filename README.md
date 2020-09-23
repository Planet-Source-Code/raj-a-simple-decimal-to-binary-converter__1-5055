<div align="center">

## Simple Decimal To Binary Converter


</div>

### Description

This simple code will convert the Long Integers to it's binary Equivalent...
 
### More Info
 
Long Integers ( positive ) 1 - 999999999

This program is not capable of accepting negative numbers or numbers which are more than 999999999

if the range is met then this will return the Binary equivalent...

if the input is either non-numeric or not in range ( 1 - 999999999 ) then

it won't continue.....


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Raj A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/raj-a.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/raj-a-simple-decimal-to-binary-converter__1-5055/archive/master.zip)





### Source Code

```
Option Explicit
'********************************************'
'***This Function is to just to Return the***'
'***Binary Equivalent for Any long integer***'
'********************************************'
Private Sub Command1_Click()
  Dim str1 As String
  On Error GoTo a:
  str1 = cBin(CLng(Text1.Text))
  MsgBox str1
  Exit Sub
a:
End Sub
Public Function cBin(a As Long) As String
  Dim bal As Long
  Dim str1 As String
  bal = a
    Do Until a <= 0
      bal = a Mod 2
      If bal = 0 Then
        a = a / 2
      Else
        a = (a - 1) / 2
      End If
      str1 = str1 & CStr(bal)
    Loop
    cBin = StrReverse(str1)
End Function
```

