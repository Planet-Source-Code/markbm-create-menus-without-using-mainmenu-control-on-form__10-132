<div align="center">

## Create menus without using mainmenu control on form


</div>

### Description

This example will create simple menu on form without using mainmenu control.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[markbm](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/markbm.md)
**Level**          |Beginner
**User Rating**    |4.0 (20 globes from 5 users)
**Compatibility**  |VB\.NET
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__10-3.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/markbm-create-menus-without-using-mainmenu-control-on-form__10-132/archive/master.zip)





### Source Code

```
' Create an empty MainMenu.
 Dim mainMenu1 As New MainMenu()
 Dim menuItem1 As New MenuItem("&File")
 Dim menuItem2 As New MenuItem()
 Dim menuitem3 As New MenuItem()
 Dim menuItem5 As New MenuItem("&Help")
 Dim menuitem6 As New MenuItem()
 ' Set the caption for the first submenu.
 menuItem2.Text = "&Open"
 menuitem3.Text = "E&xit"
 ' set the caption for second submenu
 menuitem6.Text = "&About"
 ' Add menuItem2 and menuItem3 to menuItem1's list of menu items.
 menuItem1.MenuItems.Add(menuItem2)
 menuItem1.MenuItems.Add(menuitem3)
 ' Add menuItem6 to menuItem5's list of menu items.
 menuItem5.MenuItems.Add(menuitem6)
 ' Add two MenuItem objects to the MainMenu for displaying.
 mainMenu1.MenuItems.Add(menuItem1)
 mainMenu1.MenuItems.Add(menuItem5)
 AddHandler menuItem2.Click, AddressOf Me.Item1_Click 'handles the menuitem2 click
 AddHandler menuitem3.Click, AddressOf Me.Item2_Click 'handles the menuitem3 click
 AddHandler menuitem6.Click, AddressOf Me.Item3_Click 'handles the menuitem6 click
 Me.Menu = mainMenu1
 End Sub
 Private Sub Item1_Click(ByVal sender As Object, ByVal e As System.EventArgs)
 MessageBox.Show("You clicked the open menu.")
 End Sub
 Private Sub Item2_Click(ByVal sender As Object, ByVal e As System.EventArgs)
 MessageBox.Show("You clicked the exit menu.")
 End
 End Sub
 Private Sub Item3_Click(ByVal sender As Object, ByVal e As System.EventArgs)
 MessageBox.Show("You clicked the About menu.")
 End Sub
```

