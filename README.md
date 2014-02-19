untwister
=========

Untwister, Multi-threaded seed recovery tool for PRNGs

Usage:
```
untwister -i <input_file> [-d <depth> ] [-r <rng_alg>] [-g <seed>] [-t]

	-i <input_file>
		Path to file input file containing observed results of your RNG. The contents
		are expected to be newline separated 32-bit integers. See test_input.txt for
		an example.
	-d <depth>
		The depth (default 1000) to inspect for each seed value when brute forcing.
		Choosing a higher depth value will make brute forcing take longer (linearly), but is 
		required for cases where the generator has been used many times already.
	-r <rng_alg>
		The RNG algorithm to use. Supported RNG algorithms:
			mt19937 (default)
			glibc-rand
	-t
		Use bruteforce, but only for unix timestamp values within a range of +/- 1 
		year from the current time.
	-g <seed>
		Generate a test set of random numbers from the given seed (at a random depth)
```

