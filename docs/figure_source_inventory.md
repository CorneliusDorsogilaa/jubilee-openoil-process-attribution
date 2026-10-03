# Figure source inventory

This record maps each submitted main-manuscript and Supporting Information figure to the archived source data and the analysis or plotting code needed to reproduce it.

The machine-readable version is `metadata/figure_source_inventory.csv`.

## Main manuscript

| Figure | Source-data state | Current archived source | Remaining action |
|---|---|---|---|
| Fig. 1 | Partial | `derived_data/Fig1_reference_annotation_metrics.csv`; authoritative production runner | Add the final map-building script and either the four reference production NetCDFs to Zenodo or an exported trajectory/geometry table sufficient to redraw the map. |
| Fig. 2 | Source tables present | `Figure2_ensemble_absolute_metrics.csv`, `Figure2_paired_A90_changes.csv` | Add final figure-building script. |
| Fig. 3 | Partial | `Fig3_revised_vertical_depth_ensemble.csv`; M9 depth-analysis script | Add `Fig3_revised_vertical_timeseries.csv`, M9 per-seed/summary outputs, and final figure-building script. |
| Fig. 4 | Source table present | `Fig4_revised_C3_fate_timeseries.csv` | Add final figure-building script. |
| Fig. 5 | Source table present | `Fig5_revised_weathering_entrainment_mechanism.csv`; corrected M8 reconstruction script | Add the M8 diagnostic CSV/summary and final figure-building script. |
| Fig. 6 | Compact source tables present | `Fig6_timestep_screen.csv`, `Fig6_particle_count_ensemble.csv` | Add the M4 per-seed/summary/paired outputs and final figure-building script. |

## Supporting Information

| Figure | Source-data state | Current archived source | Remaining action |
|---|---|---|---|
| Fig. S1 | Regenerable from archived audit script | R3 audit script | Add well-mixed summary, histogram and diffusivity-profile CSVs. |
| Fig. S2 | Partial | R3 audit script | Add wind-threshold occupancy and lag-correlation CSVs plus `Fig3_revised_vertical_timeseries.csv`. |
| Fig. S3 | Summary tables present | `FigS3_oil_sensitivity_summary.csv`, `FigS3_oil_property_summary.csv`; M10 analysis script | Add M10 properties/metrics CSVs. Panels c–d also need per-element Qua Iboe/Bonny output, either as compact extracted CSVs or through the corresponding reference NetCDFs in Zenodo. |

## Archive principle

GitHub contains scripts and compact derived tables. Large simulation outputs may be deposited in the Zenodo release if needed for full figure regeneration. ERA5 and GLORYS forcing products are not redistributed; their provenance and retrieval details are documented separately.

The final SHA256 manifest must be regenerated only after this inventory is complete and the exact submission-matched files are frozen.
