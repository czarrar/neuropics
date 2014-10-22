neuropics
=========

Generates PNG images from 2D brain slices. Can optionally overlay statistical images or overlay an outline of a brain image. This is a wrapper around FSL's overlay, slicer, and pngappend commands.

## Output of Help

### optional arguments:

```
  -h, --help            show this help message and exit
```

### Positional Arguments:

```
  input                 Input 3D brain image
  output                Output 2D PNG image
```

### Overlay Inputs:

```
  --edge-overlay FILE   An outline of a brain image is overlaid on the input
                        (useful for checking registration). Note: the overlay
                        options don't apply to this input.
  --overlay file min max
                        image to overlay on input
  --overlay2 file min max
                        2nd image to overlay on input
  --show-negative       Will take the 1st overlay and threshold it to have a
                        negative range (this would be useful if you wanted to
                        display positive & negative thresholded maps). Note:
                        you can't specify both the --overlay2 and this option.
```

### Overlay Options:

```
  Note: these only apply to --overlay and --overlay2

  -t, --transparency    make overlay colors semi-transparent
  --checkerboard        use checkerboard mask for overlay
  --background-range min max
                        setting range of underlay, only used when overlay
                        option has been given (default: automatic estimation)
```

### Main Image Options:

```
  --slice-labels
  --lut color           use a different colour map from that specified in the
                        header
  --scale positive-#    relative size of each slice
  --intensity min max   specify intensity min and max for display range
  --no-lr-labels
```

### Output Image Options:

```
  -s slice_name, --slice slice_name
                        type of slice; can be: a/axial, c/coronal, or
                        s/sagittal
  -w slices, --width slices
                        image width in # of slices
  -l slices, --height slices
                        image height in # of slices
  -e number, --slice-every number
                        include every X # of slice
```

### Miscellaneous Options:

```
  --force               overwrite output if it exists
  -v, --verbose
  --dry-run             Won't execute anything but prints what would have been
                        executed
  --version             show program's version number and exit
```
