# SUEWS Hackathon Practice Setup

This is a public setup page for AashniTanna's SUEWS Community Hackathon practice repository.

## Setup Status

- Repository created from `UMEP-dev/suews-hackathon-template`.
- Task brief read and summarised for setup planning.
- `suews@suews` plugin installed and used to bootstrap SUEWS/SuPy tooling.
- A bundled SUEWS KCL/London sample case was initialised, validated, run, diagnosed, and summarised.
- This page is intended as a setup smoke test, not a real heat-risk submission.

## Example SUEWS Run

The example run is in `analysis/suews-example/`.

- Config: `analysis/suews-example/sample_config.yml`
- Forcing: `analysis/suews-example/Kc_2012_data_60.txt`
- Output: `analysis/suews-example/Output/KCL1_2012_SUEWS_60.txt`
- Provenance: `analysis/suews-example/Output/provenance.json`
- Diagnostics: `analysis/suews-example/Output/diagnostics.json`
- Summary: `analysis/suews-example/Output/summary.json`

The readiness check says this case is not a real site setup: location, land-cover fractions, and forcing are still the bundled KCL/London sample defaults. That is acceptable for a setup smoke test, but those values must be replaced for the actual hackathon city.

## Diagnostic Note

The diagnostic pass found output files, provenance, and zero NaN fractions for `QH`, `QE`, and `QN`. It also reported an energy-balance closure warning:

> Mean closure residual 7.283 exceeds 0.10.

I am leaving that warning visible because the purpose here is to confirm the workflow and surface caveats honestly.

## SUEWS Citation Reminder

The final hackathon submission should cite:

- Jarvi, L., Grimmond, C.S.B. and Christen, A. (2011). The Surface Urban Energy and Water Balance Scheme (SUEWS): Evaluation in Los Angeles and Vancouver. Journal of Hydrology, 411(3-4), 219-237. https://doi.org/10.1016/j.jhydrol.2011.10.001
- Ward, H.C., Kotthaus, S., Jarvi, L. and Grimmond, C.S.B. (2016). Surface Urban Energy and Water Balance Scheme (SUEWS): Development and evaluation at two UK sites. Urban Climate, 18, 1-32. https://doi.org/10.1016/j.uclim.2016.05.001
