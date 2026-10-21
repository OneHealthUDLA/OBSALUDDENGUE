# Ecuador national dengue surveillance records, 2021–2025 (MoH extract)

Companion data for: *Recorded laboratory confirmation in Ecuador's national dengue surveillance data, 2021–2025: completeness and heterogeneity across years, provinces and health providers* (OBSALUD; PLOS Global Public Health, PGPH-D-26-02929, under revision).

Source: Ministerio de Salud Pública del Ecuador, dengue surveillance database extract obtained by OBSALUD through a public-information request; also published at https://obsalud.org/biblioteca/bases-de-datos-abiertos/base-dengue-descarga/. No personal identifiers.

## Files
| File | Content |
|---|---|
| `dengue_surveillance_ecuador_2021_2025_records.csv` | All 58,793 records as received (160,660 reported cases) plus two added columns: `excluded_from_analysis` (1 = excluded) and `exclusion_reason`. |
| `dengue_surveillance_ecuador_2021_2025_analytic.csv` | Analytic dataset: 58,750 records, 160,617 cases (epidemiological week 1/2021 to week 36/2025). 43 records assigned to weeks 50–52 of 2025 are excluded because they post-date the extraction. |
| `summary_by_year.csv`, `summary_by_institution.csv`, `summary_by_province.csv` | Aggregated tables with Wilson 95% CIs (manuscript Tables 1–2, S1 Table). |
| `weekly_series.csv` | Weekly counts used for Fig 1. |
| `analysis_code.py` | Reproduces all numbers: `python analysis_code.py dengue_surveillance_ecuador_2021_2025_analytic.csv`. |

## Data dictionary (original MoH column names)
| Column | Description |
|---|---|
| `Año`, `Semana` | Epidemiological year and week of notification (2021 has 53 weeks in the source calendar). |
| `Institucion` | Reporting institution: MSP (Ministry of Public Health), IESS, ISSPOL, ISSFA, JUNTA DE BENEFICENCIA, SOLCA, PRIVADO, ONG, MUNICIPIO. |
| `Unidad operativa`, `Unicodigo` | Notifying facility name and unique code. |
| `Cod_Provincia`, `Provincia`, `Cod_Canton`, `Canton`, `Cod_Parroquia`, `Parroquia` | Location of the notifying facility. |
| `Evento` | `A90X` = dengue without warning signs (aggregate notification); `A91X` = dengue with warning signs or severe dengue (individual notification). |
| `Total_casos` | Cases in the record (always 1 for A91X; 1–100 for aggregate A90X rows). |
| `Confirmado_laboratorio` | 1 = recorded laboratory confirmation; 0 = none recorded. Only populated for A91X. Absence of a recorded confirmation does not imply that no test was performed. |
| `Tipo_prueba` | 0 = none recorded; 1 = PCR; 2 = other (non-molecular) test. The extract does not distinguish NS1, IgM/IgG, paired serology or rapid tests, and contains no specimen or result dates. |

## Known limitations
No unique record identifier (identical A91 rows cannot be distinguished from duplicates); no serotype field; 2025 incomplete (weeks 1–36); administrative surveillance data subject to reporting delay and post-closure updates.

Encoding: UTF-8, comma-separated. Licence: as per OBSALUD open-data terms.
