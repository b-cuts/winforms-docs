---
title: RadControl Testing Considerations
page_title: RadControl Testing Considerations | UI for WinForms Documentation
description: RadControl Testing Considerations
slug: winforms/telerik-presentation-framework/layout/radcontrol-testing-considerations
tags: radcontrol,testing,considerations
published: True
position: 11
previous_url: tpf-layout-radcontrol-testing-considerations
---

# RadControl Testing Considerations

When writing unit tests it's often convenient to use a RadControl, not as a child of a form, but standalone. This makes for faster performance and simplicity of the test setup and tear-down methods. Whenever a property having an effect on element size or children arrangement is changed explicitly, a request to the layout system is added to the queue of events to be processed. In order to force the processing of this change in layout, the __UpdateLayout()__ method has to be called on the element in question.
