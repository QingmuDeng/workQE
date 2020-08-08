# Basic Silicon

`wget http://www.crystallography.net/cod/9008566.cif?CODSESSION=er5ih98t6glolb91ha5hqae8ta`

`cif2cell  9008566.cif -p quantum-espresso -o basic.in`

```
&CONTROL
  calculation='scf',
  outdir='.',
  prefix='basic',
  pseudo_dir='.',
  verbosity='low',
  tprnfor=.true.,
  tstress=.true.,
/
```

```
&SYSTEM
  ibrav = 0
  A =    5.43070
  nat = 2
  ntyp = 1
  ecutwfc=50,
  ecutrho=200,
  input_dft='pbe',
  occupations='smearing',
  smearing='mv',
  degauss=0.005d0,
/
```
```
&ELECTRONS
    conv_thr=1d-08,
    mixing_beta=0.7d0,
/
```
`wget http://www.quantum-espresso.org/upf_files/Si.pbe-n-kjpaw_psl.1.0.0.UPF`
```
ATOMIC_SPECIES
  Si   28.08500  Si.pbe-n-kjpaw_psl.1.0.0.UPF
```
After the atomic positions, add these lines (we will call this the k-mesh later on):
```
K_POINTS {automatic}
7 7 7 0 0 0
```

`pw.x -input basic.in > basic.out`