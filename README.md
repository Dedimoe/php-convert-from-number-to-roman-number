# php-convert-from-number-to-roman-number
Conversion from decimal to roman number

create file roman.php in doc root apache :

```
<?php

function toRoman($n) {
    $a = array('M' => 1000, 'CM' => 900, 'D' => 500, 'CD' => 400, 'C' => 100, 'XC' => 90, 
    'L' => 50, 'XL' => 40, 'X' => 10, 'IX' => 9, 'V' => 5, 'IV' => 4, 'I' => 1);
    $r = '';
    while ($n > 0) {
        foreach ($a as $roman => $i) {
            if($n >= $i) {
                $n -= $i;
                $r .= $roman;
                break;
            }
        }
    }
    return $r;
}

echo toRoman(22);
```

Usage in browser :
```
http://localhost/roman.php
```

The output :
```
XXII
```
