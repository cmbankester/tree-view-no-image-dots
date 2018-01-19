# The Problem

There is no way to set an image for some nodes of a WinForms TreeView control but not others.

See [this StackOverflow post](https://stackoverflow.com/questions/261660/how-do-i-set-an-image-for-some-but-not-all-nodes-in-a-treeview) for more info.

# The Solution

Add an image of just dots to extend the TreeView dots all the way to the control.

See [the answer given on StackOverflow](https://stackoverflow.com/a/20616195/400461).

Drop the [no-image-dots.png](no-image-dots.png) file into the ImageList used by your TreeView (assuming your ImageList#ImageSize is 16x16 px) as the first image. For any `Node n` that you don't want an image on, just set `node.SelectedImageIndex = 0` and `node.ImageIndex = 0`.
