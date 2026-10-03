# Figure source inventory

This record maps each submitted main-manuscript and Supporting Information figure to the archived source data and the analysis or plotting code needed to reproduce it.

The machine-readable version is `metadata/figure_source_inventory.csv`.

## Curation decision

The uploaded figure-source collection was audited. The authoritative final plotting scripts are:

- Fig. 1: script 27, `figure1_production_map_pub`; scripts 26 and 28–32 are superseded alternatives and are not part of the submission archive.
- Fig. 2: `scripts/figures/build_Fig2_ensemble_process_attribution.py`.
- Fig. 3: script 77.
- Fig. 4: script 85.
- Fig. 5: script 87.
- Fig. 6: script 88b; script 88 is superseded because 88b robustly identifies files using the actual NetCDF trajectory count.

The diagnostics supplied with the collection contain all requested R3, M4, M8, M9 and M10 source CSVs. A curated upload package has therefore been reduced to the authoritative scripts and diagnostics only.

## Main manuscript

| Figure | Source-data state | Current archived source | Remaining action |
|---|---|---|---|
| Fig. 1 | Compact export utility ready | `derived_data/Fig1_reference_annotation_metrics.csv`; production runner; `scripts/archive/90_export_compact_archive_sources.py` | Add `archive_sources/Fig1_reference_plot_source.csv.gz` from the final upload bundle; it contains the 250 plotted trajectories per configuration plus all final positions. Add the authoritative script-27 map builder from the same bundle. |
| Fig. 2 | Complete | `Figure2_ensemble_absolute_metrics.csv`, `Figure2_paired_A90_changes.csv`, and `scripts/figures/build_Fig2_ensemble_process_attribution.py` | None. |
| Fig. 3 | Diagnostics verified in curated package | `Fig3_revised_vertical_depth_ensemble.csv`; M9 analysis script | Add `Fig3_revised_vertical_timeseries.csv`, M9 per-seed/summary outputs, and the script-77 figure builder from the curated package. |
| Fig. 4 | Figure-source table complete; builder verified | `Fig4_revised_C3_fate_timeseries.csv` | Add the script-85 figure builder from the curated package. |
| Fig. 5 | Figure-source table complete; diagnostics/builder verified | `Fig5_revised_weathering_entrainment_mechanism.csv`; corrected M8 reconstruction script | Add `M8_mechanism_timeseries.csv` and the script-87 figure builder from the curated package. |
| Fig. 6 | Compact source tables complete; diagnostics/builder verified | `Fig6_timestep_screen.csv`, `Fig6_particle_count_ensemble.csv` | Add M4 per-seed/summary/paired outputs and the script-88b figure builder from the curated package. |

## Supporting Information

| Figure | Source-data state | Current archived source | Remaining action |
|---|---|---|---|
| Fig. S1 | Diagnostics verified in curated package | R3 audit script | Add well-mixed summary, histogram and diffusivity-profile CSVs from the curated package. |
| Fig. S2 | Diagnostics verified in curated package | R3 audit script | Add wind-threshold occupancy and lag-correlation CSVs plus `Fig3_revised_vertical_timeseries.csv` from the curated package. |
| Fig. S3 | Summary/variability sources complete; compact exporter ready | `FigS3_oil_sensitivity_summary.csv`, `FigS3_oil_property_summary.csv`, `FigS3_reference_variability.csv`; M10 analysis script; compact exporter | Add M10 properties/metrics CSVs and `archive_sources/FigS3_per_element_surface_time.csv.gz` plus `archive_sources/FigS3_reference_offsets.csv` from the final upload bundle. |

## Raw NetCDF decision

The final public archive will **not** redistribute the large raw OpenOil NetCDF outputs. Instead it will contain:

1. the exact run configuration and authoritative analysis scripts,
2. complete compact figure-source tables,
3. per-seed/diagnostic summaries used in the paper,
4. compact trajectory/per-element exports for the two figures that otherwise require reference NetCDFs.

This keeps the archive lightweight while preserving figure reproducibility. A full model rerun still requires the externally licensed ERA5 and GLORYS forcing products, which are not redistributed and are documented by provenance/retrieval information.

The final SHA256 manifest must be regenerated only after the curated figure-source files and compact exports are committed.
