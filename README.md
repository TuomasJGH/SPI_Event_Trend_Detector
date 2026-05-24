# SPI Event Trend Detector

**Author:** Tuomas Haapala  
**Contact:** tuomas.haapala@aalto.fi
**Organization:** Aalto University
**Website:** https://github.com/TuomasJGH/SPI_Event_Trend_Detector

## Project Overview
This project detects trends in precipitation events based on the Standardized Precipitation Index and standard and modified Mann-Kendall trend tests.
.
* problem statement: why does your research matter
* problem statement: what overarching theoretical, applied, societal, environmental problem does your research address? 
* challenge statement: why has this problem not been solved before?
* solution statement: what specific element of the challenge does your research resolve?
* objective: how will you accomplish this?
* literature review: focus on foundational or methods papers that closely describe your analytical workflow.
* research questions: focus on testable hypothesis, even if you're not a frequentist. 


## Data Sources

Describe your study area, and period of interest. Specify whether training data represents a different location/time period than forecast simulations. Detail the temporal and spatial frequency of your process.

This project uses openly available gridded precipitation data provided by the Finnish Meteorological Institute. The data is in the form of NetCDF grid files, where each file contains a year's daily precipitation time series in each cell. Grid size is 1147*661, and values outside Finland are masked.

Data is currently available for years 1961 to 2025, with updates adding data for the current year.  

### Published Data Sources
| Name | Source | Description | Access Method | URL | Details | Citation |
|------|--------|-------------|---------------|--------------|---------|---------------|
| rrday_(year).nc | Finnish Meteorological Institute | Yearly grids containing daily precipitation data for Finland | Direct access via URL | [URL](http://fmi-gridded-obs-daily-1km.s3-website-eu-west-1.amazonaws.com/) | Spatial resolution: 1 km2, EPSG:3067 projection | Finnish Meteorological Institute. (2026) Daily observations in 1km*1km grid. Available from: [http://fmi-gridded-obs-daily-1km.s3-website-eu-west-1.amazonaws.com](http://fmi-gridded-obs-daily-1km.s3-website-eu-west-1.amazonaws.com) |
### Data Access Notes
In the "How to Reproduce," descripe how to configure automatic access control mechanisms for each data source. 

### Inputs folder
Any direct data download links can be pasted into the "datalinks.txt" file in the inputs folder. Specify which dataset links can be accessed via the datalinks.txt folder. Note: this should only be used for PDIs: if the url changes, it will break the reproducibility of your workflow.

Detail any datasets that are in your inputs data folder. Note this is only for data that is too small/trivial to be published: **no files greater than 10 MB can be stored in repository**. Examples might include spatial polygons that have undergone geometry simplification for API searches, text-based keys mapping variable names to integer values, etc.

## Methods Summary

**Model Framework:** 
Describe steps involved in data preprocessing

## Repository Structure

| Folder/File | Description |
|-------------|-------------|
| notebooks/ | SE1–SE4 notebooks |
| inputs/ | minimal input data required, note most data should be stored on OGC/FAIR compliant databases and accessed from stable URLs |
| ../raw_data/ | data downloaded from stable URLs/PDIs |
| ../processed_data/ | analysis-ready datasets |
| model_data/ | Saved model outputs, model configuration files, predictions|
| figures/ | Figures, tables, graphs, and data-derivatives (e.g. summary statistics) displayed in manuscript text |
| run_reproducibility.py | Reproducibility wrapper |
| Dockerfile | Reproducible container |
| CITATION.cff | Citation metadata, sourced directly from Zenodo |

## How to Reproduce

### Computational requirements
What operating system, processor type, and processor specifications (RAM, cores, etc).

If GPU processing, specify CUDA version.

### Data access configurations
Describe in detail any access control mechanisms that need to be configured for an individual user to access data (e.g. tokens, cookies, certificates, URL customization). Provide links to documentation.

### Run the code
```bash
pip install -r requirements.txt
python run_reproducibility.py
```
## Results

Display key figures in `/figures` folder, with description:

![Example](figures/example.png)

## Citation

If you use this software, please cite:

**APA format**

Tuomas Haapala (2026).
*SPI Event Trend Detector* (Version 0.1.0).
Aalto University.
DOI: 

**BibTeX**

```bibtex
@software spi_event_trend_detector,
  author = Tuomas Haapala,
  title = SPI Event Trend Detector,
  year = 2026,
  version = 0.1.0,
  doi = ,
  url = https://github.com/TuomasJGH/SPI_Event_Trend_Detector
}
```
or

[![DOI](https://zenodo.org/badge/DOI/DOI_PENDING.svg)](DOI_PENDING)

## License

MIT

## Contribution Guidelines
Contributions that improve the quality, clarity, and reproducibility of this project are welcome.
* Open an issue before making major or result-affecting changes.
* Keep pull requests focused and clearly describe what changed and why.
* Follow existing code style and update documentation as needed.
* Do not modify code or data used to reproduce published results without discussion.
* Ensure workflows remain reproducible (environment, dependencies, random seeds).
* Do not commit large or restricted datasets; respect data licenses.
By contributing, you agree that your work will be released under the project’s license.

## Notes:
Focus on graphically rich, interactive elements to communicate your research to diverse stakeholders.
[Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet) 
