# Copy module

Although passing around references is often the handiest way to deal with lists and dictionaries, if the function modifies the list or dictionary that is passed, you may not want these changes in the original list or dictionary value. For this, Python provides a module named copy that provides both the copy() and deepcopy() functions. The first of these, copy.copy(), can be used to make a duplicate copy of a mutable value like a list or dictionary, not just a copy of a reference

If the list you need to copy contains lists, then use the copy.deepcopy()function instead of copy.copy(). The deepcopy() function will copy these inner lists as well.
