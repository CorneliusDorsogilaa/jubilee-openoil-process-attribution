# Required checks before Zenodo DOI release

Do **not** tag the final `v1.0.0-paper-submission` release until these are complete.

1. Update manuscript/SI timestep wording everywhere: C3 timestep screen, N=2000, Kh=100 m² s⁻¹, 5/10/15/30 min, three seeds. Production remains N=1000.
2. Regenerate or relabel manuscript Fig. 6 so panel (a) matches the verified timestep campaign description.
3. Replace Jubilee property sourcing with the final verified primary-source wording selected for the paper; keep the table temperature bases explicit.
4. Use the 2009 ERM/Tullow Jubilee Phase 1 EIS as the direct source for the 500-run stochastic OILMAP statement if that claim remains.
5. Keep Carvalho et al. (2025) only for the specific oil-property / evaporation sensitivity claim it actually supports.
6. Replace this staging `environment.yml` with the exact final environment export or add an exact package lock file.
7. Add the complete final figure-source CSV inventory and any small, redistribution-safe diagnostic outputs.
8. Decide whether raw OpenOil result NetCDFs belong in Zenodo (recommended if size/licensing permit); do not put forcing products in GitHub.
9. Recompute `metadata/file_manifest_sha256.csv` after all files are final.
10. Change `CITATION.cff` version from 0.9.0 to 1.0.0 and create GitHub release `v1.0.0-paper-submission`.
11. Archive that release in Zenodo, obtain DOI, then insert DOI into the manuscript and SI.
