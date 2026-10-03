# Required checks before Zenodo DOI release

Do **not** tag the final `v1.0.0-paper-submission` release until these are complete.

## Closed

- [x] Timestep description corrected everywhere to the verified C3 screen at **N = 2000**, **Kh = 100 m² s⁻¹**, 5/10/15/30 min, three seeds; production remains **N = 1000**.
- [x] Main-manuscript Fig. 6 caption corrected to describe the preliminary three-seed timestep screen.
- [x] Jubilee property sourcing upgraded to the official **Tullow 2019 Jubilee assay** as the primary reference; Appenteng et al. (2013) retained only as an earlier independent characterization.
- [x] Stochastic OILMAP precedent sourced directly to the **2009 Jubilee Field Phase 1 EIS**, which documents 500 independent simulations per scenario.
- [x] Carvalho et al. (2025) narrowed to the specific API-gravity / evaporation sensitivity claim it supports.
- [x] Mixed-unit temperature wording corrected so the archived final Kelvin-scale record is described as an archive property rather than a general OpenDrift behavior.
- [x] Public GitHub repository created under **CorneliusDorsogilaa**.

## Still required before Zenodo

- [x] Replace the staging environment record with the verified portable `environment.yml` and add `environment_exact.yml` as the exact executed environment snapshot (local `prefix:` removed).
- [ ] Add the complete final figure-source CSV inventory and any small redistribution-safe diagnostic outputs.
- [ ] Decide whether selected raw OpenOil result NetCDFs belong in Zenodo; do **not** redistribute ERA5 or GLORYS forcing products in GitHub.
- [ ] Recompute `metadata/file_manifest_sha256.csv` after every final repository change.
- [ ] Change `CITATION.cff` version from `0.9.0` to `1.0.0`.
- [ ] Create GitHub release `v1.0.0-paper-submission`.
- [ ] Enable the repository in Zenodo, archive the tagged release, obtain the DOI, and insert that DOI into the main manuscript and Supporting Information.
