## Changing k-mesh
we want a convergence pressure with the shortest run time possible. The goal is to find the best sized mesh with precision and computational efficiency.
|k-mesh|Hydrostatic pressure (kbar)|Runtime(s)|
|---|---|---|
|1x1x1|243.81|6.3|
|3x3x3|3.02|9.6|
|5x5x5|1.23|13.3|
|7x7x7|1.09|19.9|
|9x9x9|1.12|30.7|
|11x11x11|1.13|46.1|
`7x7x7` is therefore the best.

## Basis Function Size
After a certain point, adding more basis functions to the series won't change the overall summation very much.


## ML Search for parameter
Visit (JARVIS-ML)[https://www.ctcms.nist.gov/jarvisml/].
```
    my 3d material
 1.0
  0.000000000000000   2.820280000000000   2.820280000000000
  2.820280000000000   0.000000000000000   2.820280000000000
  2.820280000000000   2.820280000000000   0.000000000000000
  Cl  Na
   1   1
Direct
  0.500000000000000   0.500000000000000   0.500000000000000 
  0.000000000000000   0.000000000000000   0.000000000000000 

```

## M