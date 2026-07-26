# Fibonacci Spiral Algorithm (v6B)

A sparse geometric sampling algorithm that analyzes data using Fibonacci-indexed positions instead of dense sequential scans.

## Overview

Rather than reading every element of an input, the algorithm samples only Fibonacci sequence positions.

Current implementation:

* Samples **65 positions** from a **50,000-element** input (**0.13%**)
* Samples **79 positions** from a **500,000-element** input (**0.016%**)
* Runtime of approximately **0.07–0.13 ms** (independent reimplementation)
* Independent testing found the selected positions recover a global numeric statistic approximately **12–25×** more accurately than random sampling using the same sampling budget

## Dual-1 Geometry

The algorithm distinguishes the two consecutive ones in the Fibonacci sequence:

```
0, 1a, 1b, 2, 3, 5, 8...
```

where:

* **1a (Primal Spark)** represents the transition from absence to existence.
* **1b (Mirror)** represents the first observable state.

This conceptual framework was inspired by historical number-philosophy traditions—including Pythagorean thought, Kabbalah, Christian mysticism, Rosicrucian writings, and the numerological discussions of Manly P. Hall.

These ideas motivated the algorithm's geometric design. Performance claims are based solely on the documented experiments presented in the accompanying paper.

## Documentation

See **Fibonacci_Spiral_v6B_FINAL_VERIFIED.pdf** for:

* Independent verification
* Benchmark methodology
* Structural recovery experiments
* Comparisons with dense algorithms
* Metric definitions
* Reproducibility notes

The earlier "coverage efficiency 0.67–0.70" metric has been withdrawn because it does not correspond to the published v6B implementation.

## Research Status

* Original research
* Preliminary
* Not yet peer reviewed
* Core experiments reproducible using random seed 42

## License

Licensed under the **Apache License 2.0**. See the LICENSE file for details.

## Disclaimer

The conceptual origin of this work draws inspiration from historical mathematical and philosophical traditions concerning the Fibonacci sequence. The empirical evaluation is independent of those interpretations. All performance claims refer only to the experiments documented in the accompanying paper.

## Author

**Sensufrog**
Independent Researcher
June 2026
