# TephiPair downloads

[**Download the complete four-bundle handoff — 263.1 MB**](https://github.com/saifal525/tephipair-downloads/releases/tag/rashid-handoff-2026-10-22)

Open the release and download **Rashid_TephiPair_All_Four_Bundles_20261022.zip**
under Assets. This public repository and its published release assets can be
downloaded without signing in or requesting repository access.

The handoff contains:

| Bundle | Contents | ZIP size |
|---|---|---:|
| 01 | Windows app 0.1.1 with date-filename fix and synthetic TEMP examples | 108.3 MB |
| 02 | Original public IGRA archive, decoded observations, truth and metadata | 42.3 MB |
| 03 | Public GFS station extracts, retained response caches and manifests | 76.8 MB |
| 04 | Portable source, protocols, fitted regressors, reference results and instructions | 35.7 MB |

## Start on Windows

1. Extract the complete outer ZIP.
2. Extract all four numbered ZIPs into the same folder. They merge into
   `TephiPair_Public_Handoff`. Alternatively run `ASSEMBLE_BUNDLES.py` beside
   the four ZIPs using Python.
3. Read `START_HERE.txt`, then double-click `START-APP.bat`.
4. To repeat the research, use Python 3.12 and run `SETUP-RESEARCH.bat`,
   `VERIFY-HANDOFF.bat`, `REPLAY-REFERENCE.bat`, then `RETRAIN-ALL-WINDOWS.bat`.
5. Give your AI the included `AI_HANDOFF_PROMPT.txt` for project orientation,
   setup, execution and verification. Require a completed `RUN_STATUS.json`
   and passing `PARITY_REPORT.json` in each new run.

The packaged Windows app contains its own runtime; it needs no Python install.
Local TEMP viewing works offline. Live GFS refresh needs network access to NOAA.
Research setup downloads Python packages once. The supplied historical
experiment inputs are available offline. Mac/Linux source instructions are
included; native Windows software cannot run directly on those platforms.

## Public research inputs

The research weather inputs in this download come from publicly available
NOAA IGRA observations and NOAA/NCEP GFS extracts. Internal NCM TEMP archives,
COSMO material, private comparison exports, credentials and manuscripts are
excluded. This is a public-data research handoff, not a transfer of internal
observational archives. Preserve the software's original license notices;
public download availability does not relicense the application.

- [NOAA IGRA overview](https://www.ncei.noaa.gov/products/weather-balloon/integrated-global-radiosonde-archive)
- [Original station archive](https://www.ncei.noaa.gov/pub/data/igra/data/data-por/AEM00041217-data.txt.zip)
- [GFS historical archive](https://gdex.ucar.edu/datasets/d084001/)
- [Public TEMP/PILOT query](https://www.ogimet.com/sond.phtml.en)

IGRA stores decoded fixed-width sounding observations, not the original
TTAA/TTBB bulletin stream. The two included TTAA/TTBB examples are explicitly
synthetic software demonstrations, never observations or model truth. Public
encoded TEMP query coverage varies by station and date.

## Research design and limits

Compare raw GFS, forecast-only ML and current-balloon-assisted ML at +12/+24 h.

| Evaluation | Training | Early stopping |
|---|---|---|
| 2023 | 2019–2021 | 2022 |
| 2024 | 2019–2022 | 2023 |
| 2025 | 2019–2023 | 2024 |

Evaluation stops at 2025. Original reference files remain sealed; new runs
write separate outputs. No future verifying balloon is used as a predictor.
All three windows remain unqualified for operational promotion. CAPE mean
improvement does not remove CIN/LFC/moisture/coverage/uncertainty limitations;
there is no calibrated per-case confidence percentage.

Checked on Windows in independently relocated folders: exact reconstruction
of 5,123 native IGRA profiles, packaged EXE chart export, full saved-model
replay, fresh training of all 144 regressors, reference numerical parity,
and independent final ZIP assembly with 14,169 payload-file checksum checks.
Another physical computer, a clean dependency installation and Mac/Linux
numerical reproduction remain unverified. See `TESTED-HERE.txt`.

## Integrity

Full ZIP size: **263,120,240 bytes**.

SHA-256:

```text
fc41ee8b6087b36be968ec567ebe5652af3062eebf9886e7c2d47c18608a55aa
```

The release includes a checksum file and quickstart/AI instructions. The full
ZIP contains per-bundle and per-file manifests. Store the large app/data
archives as release assets rather than committing them into Git history.
