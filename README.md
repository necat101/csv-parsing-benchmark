# CSV Parsing Benchmark Lab

Benchmark comparing CSV parsing methods based on HN discussion about xsv.

## Quick Start
```bash
git clone https://github.com/necat101/csv-parsing-benchmark.git
cd csv-parsing-benchmark
python3 benchmarks/benchmark.py
```

## What It Tests
- Python csv module vs xsv vs shell tools (wc, cut, sort, awk)
- Correctness validation, not just speed
- Real CSV edge cases: quoted commas, embedded newlines, unicode, etc.

## Key Findings
- Python csv: Correct but slower (~0.015s for 10K rows)
- wc -l: Fast but WRONG on CSVs with embedded newlines
- xsv: Typically 10-100x faster than Python (when available)

See full README for HN discussion analysis and detailed results.
