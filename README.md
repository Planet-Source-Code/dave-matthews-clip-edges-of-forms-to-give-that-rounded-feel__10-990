<div align="center">

## Clip edges of forms to give that rounded feel


</div>

### Description

This code will round the edges of your form to give that clipped/rounded look.
 
### More Info
 
make sure you include this at the top:

Imports System.Drawing.Drawing2D

Setting the 'pc' value to much smaller than .17 will clip your close button. So make sure you can exit some other way (usually Alt+F4 works!)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dave Matthews](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dave-matthews.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |VB\.NET
**Category**       |[Graphics/ Sound](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics-sound__10-15.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dave-matthews-clip-edges-of-forms-to-give-that-rounded-feel__10-990/archive/master.zip)

### API Declarations

```

'//**************************************
'//
'// Name: Customized Form Shapes
'// Description:This simple piece of code
'//  demonstrates using the new cool customized
'//  form shapes feature of VB.NET !
'// Edited/Modified by David Matthews
'// Original Author: Tuncay Akbas
'//
'//This code is copyrighted and has
'// limited warranties.Please see
'// http://www.Planet-Source-Code
'// .com/xq/ASP/txtCodeId.796/lngWId
'// .10/qx/vb/scripts/ShowCode.htm
'//for details.
'//**************************************
```


### Source Code

```
Private Sub Form1_Paint(ByVal sender As Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles MyBase.Paint
 Dim Pth As New GraphicsPath(), pc As Decimal = 0.18
 Pth.AddEllipse(New Rectangle(-Me.Width * pc, -Me.Height * pc, Me.Width * (1 + 2 * pc), Me.Height * (1 + 2 * pc)))
 Me.Region = New Region(Pth)
End Sub
```

