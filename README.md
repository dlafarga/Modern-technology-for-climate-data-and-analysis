# Modern Technology for Climate Data and Analysis

A collection of Jupyter notebooks for visualizing and analyzing oceanographic climate data using Python. The tutorials cover 3D cross-section visualization, EOF (Empirical Orthogonal Function) analysis, and animated depth/zonal/meridional cross-sections — applied to both GLORYS and GODAS datasets.

Companion tutorials and detailed write-ups for each notebook are available at [dlafarga.github.io](https://dlafarga.github.io).

---

## Notebooks

### 3D Visualization — GODAS
**`3D_visualization_Tutorial(GODAS).ipynb`**

Introduces 3D cross-section visualization using freely available GODAS ocean temperature data. Covers downloading data directly from NOAA, setting up regional meshgrids, and plotting depth cross-sections with a custom colormap. Includes a full pipeline to export figures as PNGs and compile them into an animated GIF.

- Data: GODAS potential temperature (`pottmp`) from NOAA PSL
- Cross-section type: Zonal, meridional, depth
- Output: Single figures and animated GIF stepping through depth layers

---

### 3D Animation — GLORYS
**`3D_GLORYS_animation_tutorial.ipynb`**

Builds on the GLORYS visualization tutorial by animating cross-sections across multiple indices. Covers zonal, meridional, and depth cross-section animations for a specified region, with full GIF export pipelines for each.

- Data: GLORYS12 (1/12° resolution, 50 depth layers)
- Cross-section types: Zonal, meridional, depth
- Output: Animated GIFs for each cross-section type

---

### 3D EOF Plotting — GLORYS
**`3D_GLORYS_EOF_Plotting_tutorial.ipynb`**

Demonstrates how to load precomputed EOF modes and visualize them as 3D cross-sections. Covers volume weighting, land masking, and creating publication-quality 3D figures from EOF output.

- Data: GLORYS12 EOF output (included as `EOF_1.nc`)
- Cross-section types: Zonal, meridional, depth
- Output: Single and multi-panel 3D figures

---

### 3D EOF Calculation — GODAS
**`3D EOF Calc (GODAS).ipynb`**

Covers the computation of 3D EOFs from GODAS temperature data, including data preprocessing, volume weighting by latitude and depth, and saving the output for visualization.

- Data: GODAS potential temperature
- Output: NetCDF file with computed EOF modes

---

## Data

| File | Description |
|------|-------------|
| `EOF_1.nc` | Precomputed EOF mode 1 from GLORYS12, used in the EOF plotting tutorial |
| `GLORYS figures/` | Example output figures from GLORYS-based notebooks |
| `GODAS figures/` | Example output figures from GODAS-based notebooks |

GODAS data can be downloaded directly from [NOAA's Physical Sciences Laboratory](https://psl.noaa.gov/data/gridded/data.godas.html). GLORYS12 data is available through the [Copernicus Marine Service](https://marine.copernicus.eu/).

---

## Requirements

```
matplotlib
numpy
netCDF4
scipy
imageio
Pillow
```

Install all dependencies with:

```bash
pip install matplotlib numpy netCDF4 scipy imageio Pillow
```

---

## Key Features

- **Custom colormap** — a blended GnBu/hot colormap designed for ocean temperature data, providing smooth transitions from cold (blue) to warm (red/yellow)
- **Land masking** — NaN values are plotted as black to clearly distinguish ocean from land in every cross-section
- **Flexible region selection** — all functions are parameterized by index arrays, making it straightforward to zoom into any ocean basin
- **Animated GIFs** — each notebook includes a full pipeline to produce smooth animations from sequential cross-sections

---

## Related Posts

- [3D Visualization Tutorial using GLORYS](https://dlafarga.github.io/journal/3D-Visualization-Tutorial-using-GLORYS.html)
- [3D Animation using GLORYS](https://dlafarga.github.io/journal/3D-animation-using-GLORYS.html)
- [3D Visualization of GODAS Data](https://dlafarga.github.io/journal/3D-Visualization-GODAS.html)

---

## Author

**Dani Lafarga** — [dlafarga.github.io](https://dlafarga.github.io)
