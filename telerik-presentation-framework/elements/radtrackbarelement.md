---
title: RadTrackBarElement
page_title: RadTrackBarElement | UI for WinForms Documentation
description: RadTrackBarElement
slug: winforms/telerik-presentation-framework/elements/radtrackbarelement
tags: radtrackbarelement
published: True
position: 2
previous_url: tpf-elements-radtrackbar
---

# RadTrackBarElement

## 

RadTrackBarElement contains the logic and user interface for RadTrackBar. 

![tpf-elements-radtrackbar 001](images/tpf-elements-radtrackbar001.png)

{{source=..\SamplesCS\TPF\Elements\MyTrackBarControl.cs region=myTrackBarControl}} 
{{source=..\SamplesVB\TPF\Elements\MyTrackBarControl.vb region=myTrackBarControl}} 

````C#
public class MyTrackBarControl : RadControl
{
    protected override void CreateChildItems(RadElement parent)
    {
        RadTrackBarElement radTrackBarElement = new RadTrackBarElement();
        radTrackBarElement.ForeColor = Color.SkyBlue;
        radTrackBarElement.TickColor = Color.Blue;
        radTrackBarElement.BackColor = Color.LightSteelBlue;
        radTrackBarElement.Minimum = 1;
        radTrackBarElement.Maximum = 100;
        radTrackBarElement.TickFrequency = 10;
        radTrackBarElement.Value = 20;
        this.RootElement.Children.Add(radTrackBarElement);
        base.CreateChildItems(parent);
    }
}

````
````VB.NET
Public Class MyTrackBarControl
    Inherits RadControl
    Protected Overrides Sub CreateChildItems(ByVal parent As RadElement)
        Dim radTrackBarElement As New RadTrackBarElement()
        radTrackBarElement.ForeColor = Color.SkyBlue
        radTrackBarElement.TickColor = Color.Blue
        radTrackBarElement.BackColor = Color.LightSteelBlue
        radTrackBarElement.Minimum = 1
        radTrackBarElement.Maximum = 100
        radTrackBarElement.TickFrequency = 10
        radTrackBarElement.Value = 20
        Me.RootElement.Children.Add(radTrackBarElement)
        MyBase.CreateChildItems(parent)
    End Sub
End Class

````

{{endregion}}
