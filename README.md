# npy-converter

* Matrix Data Converter.
* Expand matrix for multi-thread, multi-process
* Divid matrix for multi-thread, multi-process

Support: .mtx, .npy, .npz

## Requirement

* scipy
* numpy

## Usage

### Converter

* .npy -> .npz

```bash
python3 npy2npz.py example/matrix.npy bsr|csr|coo|dia|dok|lil
```

* .npz -> .mtx

```bash
python3 npz2mtx.py example/matrix.npz
```

* .mtx -> .npz

```bash
python3 mtx2npz.py example/matrix.mtx bsr|csr|coo|dia|dok|lil
```

* .npz -> .npy

```bash
python3 npz2npy.py example/matrix.npz
```
****
### Expander

* .npy: (56, 56) -> (64, 64))

```bash
python3 expandnpy.py example/matrix.npy 16
```

* .npz: (56, 56) -> (64, 64))

```bash
python3 expandnpz.py example/matrix.npz bsr|csr|coo|dia|dok|lil 16
```

### Diveder

* .npy: (56, 56) -> 4*(16, 64))

```bash
python3 divnpy2n.py example/matrix.16.npy 4
```

* .npz: (56, 56) -> 4*(16, 64))

```bash
python3 divnpz2n.py example/matrix.16.npz 4 
```


## License

[MIT license](https://en.wikipedia.org/wiki/MIT_License)
