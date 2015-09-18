# iOS_Circle_ImageView

1. How to mask & shadown iamge, e.g. circlur profile image

   http://travisjeffery.com/b/2012/08/ios-how-to-mask-and-shadow-an-image/

2. how to get tableview indexPath when a subview is clicked ?

   http://travisjeffery.com/b/2012/07/getting-the-index-path-of-a-table-view-cell-via-a-subview-event/

3. drop a shadow for your tableview cell

(PS: or probably better it should be done in a custom view's onDraw)
   http://travisjeffery.com/b/2012/07/adding-a-drop-shadow-to-a-table-view/

4. Make dynamic height tableview cell with autolayout

http://www.raywenderlich.com/73602/dynamic-table-view-cell-height-auto-layout
Note: Add below code to your ViewController, so the tableview update its visible cells with 
correct width when screen rotates, caz in iOS, rotation won't destroy those views.

- (void)didRotateFromInterfaceOrientation:(UIInterfaceOrientation) fromInterfaceOrientation
{
    [super didRotateFromInterfaceOrientation:fromInterfaceOrientation];
    
    //This will automatically update the table cells with new width after screen rotated.
    [_tableView reloadRowsAtIndexPaths:[_tableView indexPathsForVisibleRows] withRowAnimation:UITableViewRowAnimationNone];
}
