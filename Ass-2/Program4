# Create the main window
package require Tk
wm title . "List Box Example"

# Create two list boxes and buttons
frame .frame
listbox .frame.listbox1 -selectmode single -width 20 -height 10
listbox .frame.listbox2 -selectmode single -width 20 -height 10
button .frame.addButton -text "Add Item" -command addItem
button .frame.removeButton -text "Remove Item" -command removeItem

# Pack list boxes and buttons in the frame
pack .frame.listbox1 .frame.listbox2 -side left -padx 10
pack .frame.addButton .frame.removeButton -side left -padx 5 -pady 5

# Insert some sample items into the first list box
set items {Apple Banana Cherry Date Fig Grape}
foreach item $items {
    .frame.listbox1 insert end $item
}

# Procedure to copy item from the first list box to the second
proc addItem {} {
    # Get the selected item index from the first list box
    set index [.frame.listbox1 curselection]
    if {$index ne ""} {
        # Get the selected item text
        set item [.frame.listbox1 get $index]
        
        # Add item to the second list box only if it's not already there
        if {[.frame.listbox2 get 0 end] ni $item} {
            .frame.listbox2 insert end $item
        }
    }
}

# Procedure to remove the selected item from the second list box
proc removeItem {} {
    # Get the selected item index from the second list box
    set index [.frame.listbox2 curselection]
    if {$index ne ""} {
        # Delete the selected item from the second list box
        .frame.listbox2 delete $index
    }
}

# Bind double-click events for list boxes to call the respective procedures
bind .frame.listbox1 <Double-1> {addItem}
bind .frame.listbox2 <Double-1> {removeItem}

# Run the application
pack .frame -padx 20 -pady 20
