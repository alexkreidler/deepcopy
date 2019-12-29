deepCopy
========
[![GoDoc](https://godoc.org/github.com/alexkreidler/deepcopy?status.svg)](https://godoc.org/github.com/alexkreidler/deepcopy)

DeepCopy makes deep copies of things: unexported field values are not copied.

It also allows for returning a pointer to the copied object, which is useful for using the copied object with more reflection operations.

This implementation of deepcopy is not as optimized as some other implementations (e.g. 
	[mitchellh/copystructure](https://github.com/mitchellh/copystructure)). We also don't provide benchmarks.
	
The tests probably don't work as of now because of the addition of the options.

## Usage
    cpy := deepcopy.Copy(orig, Options{ReturnPointer:false})
