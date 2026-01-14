<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/logo-light.png">
    <source media="(prefers-color-scheme: light)" srcset="docs/assets/logo-dark.png">
    <img
      alt="SolAegis logo"
      src="docs/assets/logo-light.png"
      width="220"
    />
  </picture>
</p>


<p align="center">
  The future has a heartbeat.
</p>

<p align="center">
  <img alt="Status" src="https://img.shields.io/badge/Status-Under%20Development-yellow" />
</p>


# SolAegis

SolAegis is a research-driven framework that uses dynamic knowledge graphs (DKGs)
to support heat warning monitoring, environmental exposure analysis, and
health risk modeling.

The project integrates routine clinical data with environmental and
meteorological data to enable explainable, data-driven insights for prevention,
monitoring, and resource allocation under increasing climate-related health
risks. SolAegis is developed in the context of a **planned retrospective observational research project** investigating the use of semantically enriched, interpretable dynamic knowledge graphs for environmental and cardiovascular risk modeling.

Planned institutional research settings include academic clinical research environments in Germany and international digital health research partnerships. Subject to formal ethical approval, data protection review, and governance agreements, the intended institutional context includes:

- **Charité – Universitätsmedizin Berlin**
- **Mount Sinai Digital Health Partnership**

These references are provided **solely to describe the intended research context and validation setting**.

This repository represents the public, non-sensitive project scope.
Implementation details and active pipelines are maintained in a separate
controlled-access repository during the research phase.

**Important disclaimer:**  
This repository represents the independent research work and views of the authors.  
It does **not** represent official positions, endorsements, or commitments of the above-mentioned institutions or their affiliates.

All clinical data access and processing will be subject to institutional ethics approval, data protection review, and applicable regulatory requirements.  
No patient-level clinical data are included in this repository.


## Table of contents

- [About the project](#about-the-project)
- [Research objectives](#research-objectives)
- [Environmental data integration](#environmental-data-integration)
- [Geographic normalization](#geographic-normalization)
- [Clinical study registration](#clinical-study-registration)
- [Repository scope](#repository-scope)
- [Awards](#awards)
- [Academic Visibility](#academic-visibility)
- [Data privacy and governance](#data-privacy-and-governance)
- [Project structure](#project-structure)
- [Relationship to implementation repository](#relationship-to-implementation-repository)
- [Planned public releases](#planned-public-releases)
- [Contributing](#contributing)
- [License](#license)


## About

Climate projections for Europe indicate that extreme heat events are expected to
increase substantially in both frequency and duration by the end of the century.
These trends are associated with higher risks of cardiovascular events,
dehydration, heat stroke, and excess mortality[^1].

SolAegis investigates how dynamic knowledge graphs can be used to:

- integrate heterogeneous clinical and environmental data
- model temporal exposure–outcome relationships
- support explainable and personalized risk monitoring
- improve public health preparedness and intervention planning

Rather than relying on static aggregates, SolAegis focuses on time-aware,
entity-centric representations of patients, visits, locations, and
environmental exposures.

[^1]: Source:  Heat in Germany: Health risks and preventive measures. 2023. Winklmayer et al. J Health Monit. 8(S4). 3-32.

## Research objectives

The core methodological goals of SolAegis are to:

- study the feasibility of dynamic knowledge graphs for environmental exposure modeling
- link environmental conditions to clinical timelines in a reproducible manner
- evaluate explainability and interpretability of graph-derived signals
- support retrospective observational research under appropriate governance

The project does **not** aim to replace clinical judgment or establish causal claims.


## Environmental Data Integration

SolAegis supports ingestion and normalization of **publicly available environmental data**.
These data are treated as **contextual exposure variables** and are not
interpreted as clinical outcomes.

Currently implemented or planned sources include for instance:

- **[NASA POWER (Prediction Of Worldwide Energy Resources)](https://power.larc.nasa.gov/)**  
  Daily gridded meteorological variables (e.g. temperature, humidity, wind, radiation)

- **[OpenAQ](https://explore.openaq.org/#1.2/14.1/40)**  
  Public air quality measurements from regulatory and community sensors

All environmental data are ingested with explicit provenance metadata, including:

- exact query parameters
- spatial reference
- temporal coverage
- retrieval timestamps

**Important disclaimer:** 
SolAegis is not affiliated with, endorsed by, or sponsored by NASA, OpenAQ, or any other data provider referenced. These sources are cited solely as publicly available data resources.


## Geographic Normalization

SolAegis does not rely on raw latitude and longitude coordinates as primary
identifiers.

Instead, spatial data are mapped to stable administrative regions (e.g. country, state, district)
using authoritative geographic reference services. This improves interpretability, reproducibility, and explainable
spatial reasoning in downstream graph analytics.


## Clinical Study Registration

The methodological approach implemented in SolAegis is part of a registered
retrospective observational study.

Study title:
Use of dynamic knowledge graphs in a retrospective observational study for
personalized health monitoring with routine clinical and weather data to predict
cardiovascular hospitalizations and emergencies

German Clinical Trials Register (DRKS):
https://drks.de/search/en/trial/DRKS00038327/

WHO International Clinical Trials Registry Platform (ICTRP):
https://trialsearch.who.int/Trial2.aspx?TrialID=DRKS00038327

No patient-level clinical data are included in this repository.


## Repository Scope

This public repository provides an overview of the SolAegis research project,
including objectives, governance context, and references to external standards
and registries.

Detailed methodological documentation, data processing pipelines, and analytical
implementations are maintained in a separate private repository during the
active research phase.


## Awards

- **European Universities Competition on Artificial Intelligence for Sustainable Development (Winner, 2025)**  
  Awarded for student research on AI-driven methods supporting sustainability,
  climate resilience, and health-related applications.    
  https://www.iau-hesd.net/action/european-universities-competition-artificial-intelligence-promote-sustainable-development

- **Planetary Health Poster Competition (Gold Prize Winner, 2024)**  
  Research poster recognition for methodological interdisciplinary work on
  climate-related health risk modeling.  
  https://berliner-medizinische-gesellschaft.de/


## Academic Visibility

- **European Seminar on AI for Sustainability and Climate Change (Invited, 2026)**  
  Invited project presentation on AI- and knowledge graph–based methods for
  sustainability, climate, and health-related research.  
  https://www.haw-hamburg.de/detail/news/news/show/european-seminar-on-ai-for-sustainability-and-climate-change/

- **HPI Digital Health Innovation Forum (DHIF 2025)**  
  Poster presentation on graph-based environmental and health risk modeling.
  https://hpi.de/en/hpi-digital-health-innovation-forum/dhif-2025/

- **GITEX Berlin – AI Grids Young Researcher Projects (2025)** 
  Project contribution showcasing early-stage AI and knowledge graph methods for
  sustainability- and health-related applications.

## Data Privacy and Governance

This repository will only contain:

- source code
- schema definitions
- configuration templates
- synthetic or test data where applicable

No clinical data, protected health information (PHI), or credentials are stored in Git.


## Planned Public Releases

Following completion of data access, validation, and governance review, selected
non-sensitive ingestion modules, synthetic datasets, and graph schema
documentation are planned for public release.

## Contributing

Contributions are welcome, particularly in the areas of:

- knowledge graph modeling
- environmental data processing
- reproducible research infrastructure
- documentation and methodological clarity

Please see `CONTRIBUTING.md` for contribution guidelines.

## License

This project is licensed under the Apache License Version 2.0.
