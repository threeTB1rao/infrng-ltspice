
LTSpice sim of the Infinite Noise TRNG (True Random Number Generator)

idea: https://github.com/waywardgeek/infnoise

it's basically a recursive sample-and-hold.

look at label MMOD1 or MMOD2 to see something nice.

note that 0V/0A is a fixed point for the circuit, so when you build it in hardware,
chances are it won't start, or sometimes get stuck later.

remedy: add a small NPN in inverting configuration that will inject current when
the value of - say - mmod1 gets to close to zero.

also: circuit has a bunch of op-amps and comparators not in LTSpice by default,
but they're included in the directory.

note that this circuit is excellent to learn about sample and hold, but there
are much better (and simpler) ways to generate random numbers in hardware.

