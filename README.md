# scilabCOMPlib

Port of the [constraint matrix optimization problem library](http://www.complib.de/) for [Scilab](https://www.scilab.org/).


Note that to load the benchmark matrices, you must be within the `COMPleib` directory.

## Example

Here is an example showing how a simple model often used in model reduction litterature can be loaded:

```Scilab
cd COMPleib
// Loading the data associated with the 'LAH' benchmark
[A, B1, B, C1, C, D11, D12, D21, nx, nw, nu, nz, ny] = COMPleib('LAH');
// Creating the associated linear system (e.g. for reduction)
H = syslin('c', A, B, C, 0);
w = logspace(-1, 2, 200)
bode(H,w)
```
