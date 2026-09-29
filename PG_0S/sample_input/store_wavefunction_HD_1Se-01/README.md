# Writing the wave function

## Description

The sample `inout.txt` file in this directory defines a basis of 10 ECG functions for the lowest $^1S^e$ state of the HD molecule. 
Running it generates the wave-function expansion and writes it to a separate file whose name is specified in the input (`wavefunction.txt`).

On a single CPU core, the calculation takes approximately 0.5 seconds in double precision (gfortran compiler, Intel Core i9-7900X).

## The `SAVE_HSWF` instruction

To produce the wave function, the following instruction is added to `inout.txt`:

```text
SAVE_HSWF I 10 none none none wavefunction.txt
```

The relevant arguments are:

| Argument | Description |
|---|---|
| `SAVE_HSWF` | Keyword for writing the wave function |
| `I` | Eigensolver type |
| `10` | Number of ECG basis functions |
| `wavefunction.txt` | Name of the saved wave-function file |

The basis-set size given in the `SAVE_HSWF` instruction must match the size of the wave function being saved.