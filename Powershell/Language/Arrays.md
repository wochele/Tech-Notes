# Arrays
- Collection of objects
    - Do not have to be the same type
    - Work with arrays in the pipeline
    - Can work with individual objects in an array 
- Array count starts at 0
- When an array is written to the pipeline, it's automatically enumerated
    
``` powershell
help about_arrays
```

Create an empty array:

```powershell
$array = @()
```

Create an array with a comma separated list:

```powershell
$array = 4,6,7,8,9
```

Create an array starting with a single element:

```powershell
$array = ,4 
```

Reference an individual object:

```powershell
$array[0]      #Get first element in array 
$array[-1]     #Get last element  in array 
$array[-2]     #Get second to last element in array 
$array[2..5]   #Get range of items
$array[-4..-1] #Get range of items from end of array 
```

Add items to an array:

```powershell
$array += $item  #Add item to end of array 
```

- Removing items from an array
    - Arrays are fixed size
    - No methods to remove items
    - Recreate the array with items wanted to keep

Assuming an array of values, pipe the array through Sort-Object:

```powershell
$ArrayToSort | Sort-Object
```

To modify the array:

```powershell
$ArrayToSort = $ArrayToSort | Sort-Object
```

How many objects are in the array:

```powershell
$array.count
```

Test if variable is an array:

```powershell
$array -is [array]
```

Use ForEach:

```powershell
foreach ($item in $array) {$item}
```


