# SUEWS Example Smoke Test

Purpose: confirm that the installed `suews` plugin, `suews-mcp`, SuPy, and SUEWS CLI can run end to end from the hackathon template.

## Commands Run

```sh
suews init --template simple-urban --format json analysis/suews-example
suews validate --dry-run --format json analysis/suews-example/sample_config.yml
suews run analysis/suews-example/sample_config.yml
suews diagnose --format json analysis/suews-example/Output
suews summarise --variables QN,QH,QE,QS,QF --format json analysis/suews-example/Output
```

## Result

The run completed and wrote `Output/KCL1_2012_SUEWS_60.txt` with 71 hourly records plus a header.

The saved diagnostics report 3 passing checks and 1 warning:

- Pass: `provenance.json` present.
- Pass: output file present.
- Pass: NaN fractions within 5 percent on `QH`, `QE`, and `QN`.
- Warning: mean closure residual 7.283 exceeds 0.10.

## Readiness Caveat

The `assess_readiness` check reports that this is still the bundled KCL/London sample for:

- location
- land-cover fractions
- forcing

This run is only a setup smoke test. It should not be interpreted as a heat-hazard result for the hackathon focus city.
