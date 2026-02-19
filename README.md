# ONC Echosounder Examples

This repository accompanies a conference poster on **Ocean Networks Canada (ONC) long-term echosounder data products** and provides ready-to-run examples for public use.

The poster can be found here: 
https://osm26.ipostersessions.com/Default.aspx?s=6A-29-A9-15-8D-96-A4-4C-0C-05-C6-29-3F-13-C8-7D

The goal is to make ONC bioacoustic data easier to explore by sharing:
- example `MVBS` (Mean Volume Backscatter) products,
  - The complete MVBS data products will eventually be available on Borealis (LINK COMING SOON)
- precomputed scalar time series (`CM` / center of mass and `ABC` / area backscatter),
- practical Jupyter notebooks that demonstrate analysis workflows.

## Why this repository exists

ONC has collected long-term echosounder observations across multiple coastal sites, including deployments that generate very dense raw time series (often >1 GB/day). Raw data are powerful but can be computationally expensive to download, process, and interpret.

This repository lowers that barrier by sharing value-added examples and notebook workflows that are useful for:
- interdisciplinary researchers,
- students learning time-series analysis,
- users who want a reproducible starting point before building custom pipelines.

## Conference-poster context

The examples contained in this repository focus on the exploration of:
- long-term, multi-frequency echosounder monitoring,
- cleaned MVBS products,
- descriptive scalar metrics for ecological interpretation,
- accessible open notebooks for re-use and extension.

The included examples are meant to illustrate how derived products can support analysis of diel, seasonal, and interannual variability in fish and zooplankton patterns.

## Repository contents

- `FolgerDeep_Upwelling.ipynb`  
  Demonstrates a Folger Deep workflow, including scalar time-series interpretation and optional comparison with supplementary ADCP-derived signals.
- `SaanichInlet_Overturning.ipynb`  
  Demonstrates a Saanich Inlet workflow for exploring temporal variability and notable events.
- `CM_ABC_examples/` and `CM_ABC_averaged_examples/`  
  This is the complete set of CM and ABC data products.  These scalar metric `.mat` files can be used to find interesting features in the echosounder data, and are demonstrated in the notebooks.
  - `MVBS_examples/`  
  A select number of example MVBS `.mat` files.   The full dataset will eventually be made available on Borealis. 
- `extra_data/`  
  Supplemental CSV data used by the Folger Deep notebook.

## Quick start

1. Create and activate a Python environment.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Launch Jupyter:

```bash
jupyter lab
```

4. Open a notebook from the repository root and run cells top-to-bottom.

## Dependencies

Dependencies are listed in `requirements.txt` and include scientific Python packages plus ONC client support.

## Optional ONC API access

Some notebook sections demonstrate downloading additional data through the ONC API client.

To run those sections:
1. Create/sign in to an ONC account.
2. Generate an API token from your ONC profile.
3. Replace the placeholder token in notebook cells that call `ONC(...)`.


## Data and usage notes

- Included files are example products intended for exploration, teaching, and workflow development.
- High-resolution echosounder downloads can be large and slow, depending on request size.
- File names preserve key metadata fields (site, instrument, and time window) to support traceability.

## License

Distributed under the terms in [`LICENSE`](LICENSE).
