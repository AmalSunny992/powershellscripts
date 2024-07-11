# Advanced PowerShell Scripting

## Conditional Statements and Loops
PowerShell supports various control flow constructs to handle conditional logic and iteration.

### Conditional Statements
#### If-Else

```powershell
$number = 10

if ($number -gt 5) {
    Write-Output "The number is greater than 5."
} elseif ($number -eq 5) {
    Write-Output "The number is equal to 5."
} else {
    Write-Output "The number is less than 5."
}
```

#### Switch
```powershell
$day = "Monday"

switch ($day) {
    "Monday" { Write-Output "Start of the work week." }
    "Friday" { Write-Output "End of the work week." }
    default { Write-Output "Mid-week day." }
}
```

### Loops

#### For
```powershell
for ($i = 1; $i -le 5; $i++) {
    Write-Output "Iteration $i"
}
```

#### Foreach
```powershell
$array = @(1, 2, 3, 4, 5)

foreach ($item in $array) {
    Write-Output "Item: $item"
}
```

#### While
```powershell
$count = 0

while ($count -lt 5) {
    Write-Output "Count: $count"
    $count++
}
```

#### Do-While

```powershell
$count = 0

do {
    Write-Output "Count: $count"
    $count++
} while ($count -lt 5)
```

## Functions in PowerShell
Functions allow you to encapsulate reusable blocks of code, improving modularity and readability.

Defining a Function:

```powershell
function Get-Square {
    param (
        [int]$number
    )

    return $number * $number
}

# Using the function
$square = Get-Square -number 4
Write-Output "Square of 4 is $square"
```

## Advanced Functions
You can define advanced functions with parameter validation, pipeline support, and more.

Example with Parameter Validation

```powershell
function Get-Factorial {
    [CmdletBinding()]
    param (
        [Parameter(Mandatory=$true)]
        [int]$number
    )

    if ($number -lt 0) {
        throw "Number must be non-negative."
    }

    $result = 1
    for ($i = 1; $i -le $number; $i++) {
        $result *= $i
    }
    
    return $result
}

# Using the function
$factorial = Get-Factorial -number 5
Write-Output "Factorial of 5 is $factorial"
```

#### Error Handling
PowerShell provides error handling mechanisms to manage script errors gracefully.

```powershell
try {
    # Code that might throw an exception
    $content = Get-Content -Path "nonexistentfile.txt"
} catch {
    # Handle the error
    Write-Output "An error occurred: $_"
}
```

## Conclusion
Mastering conditional statements, loops, and functions in PowerShell allows you to write more complex and efficient scripts. 
These constructs are essential for creating robust automation scripts and managing your environment effectively.
