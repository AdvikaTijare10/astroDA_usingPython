# Astronomical data analysis using python
## Stellar Classification and HR Diagram Analysis @ astroVisualize.ipynb

## Overview
This project explores stellar properties using a dataset containing temperature, luminosity, radius, absolute magnitude, star type, color, and spectral class.  
Through visual analysis and the Hertzsprung–Russell (HR) diagram, the project investigates how different star types vary in brightness, temperature, and evolutionary stage.

---

## Objectives
- Understand the relationship between temperature, luminosity, and magnitude across star types.  
- Identify patterns and outliers in stellar data.  
- Visualize star distributions using various plots.  
- Construct and interpret the **Hertzsprung–Russell (HR) diagram**.

---

## Process Summary

1. **Data Exploration**
   - Used a CSV file with features:
     - `Temperature (K)`
     - `Luminosity`
     - `Radius (relative to Sun)`
     - `Absolute Magnitude`
     - `Star Type`
     - `Star Color`
     - `Spectral Class`

2. **Visualization**
   - **Bar Graph (Matplotlib):** Number of stars by star type.  
   - **Seaborn Plot:** Star count vs. star color.  
   - **Box Plots:** Analyzed spread and outliers for temperature, luminosity, and magnitude.

3. **HR Diagram Construction**
   - Plotted **Temperature (x-axis)** vs **Absolute Magnitude (y-axis)**.  
   - X-axis decreases from left to right (as per astronomical convention).  
   - The HR diagram illustrates:
     - **Main Sequence:** Diagonal band (hot & bright → cool & dim)  
     - **Giants/Supergiants:** Upper-right region (bright but cool)  
     - **White Dwarfs:** Lower-left region (hot but dim)

---

## Observations & Learnings

- **Temperature:**  
  For types **0** and **1**, temperatures were consistent with few or no extreme outliers.

- **Luminosity:**  
  Higher-type stars exhibited more variation and numerous outliers.

- **Magnitude:**  
  Inverse relation observed — lower magnitude means brighter stars.  
  Higher-type stars (like supergiants and hypergiants) are significantly brighter.

---

## Star Type Reference

| Type | Classification | Description |
|------|----------------|--------------|
| **0** | Brown Dwarf | Small, cool, faint stars |
| **1** | Red Dwarf | Small, dim, but long-lived |
| **2** | White Dwarf | Hot, compact stellar remnants |
| **3** | Main Sequence | Ordinary stars like the Sun |
| **4** | Supergiants | Extremely bright, massive stars |
| **5** | Hypergiants | Most massive and luminous stars known |

---

## Tools & Libraries
- `pandas`
- `matplotlib`
- `seaborn`
- `numpy`

---

## Conclusion
This project deepened my understanding of stellar classification and the HR diagram.  
Visual analysis revealed how stellar temperature, brightness, and size relate to life-cycle stages — from faint brown dwarfs to radiant hypergiants.  
The HR diagram beautifully encapsulates the evolution and diversity of stars in our universe.

---


# Astronomical Image Analysis – M31 (Andromeda Galaxy) @ starVisualize.ipynb

## Overview
This project explores image retrieval, visualization, and enhancement of the Andromeda Galaxy (M31) using **Astroquery** and **Matplotlib**.  
The goal was to understand how image scaling, smoothing, and filtering techniques affect astronomical image clarity and interpretation.

---

## Objectives
- Retrieve images of M31 from different surveys and bands.
- Compare resolutions and field of view across datasets.
- Experiment with FITS file handling, scaling, and filtering.
- Visualize and interpret results through histograms and color maps.

---

## Process Summary

1. **Image Retrieval**
   - Fetched M31 images using **Astroquery.SkyView**:
     - **SDSS g-band**
     - **DSS2 Blue** (multiple pixel scales and radii for comparison)

2. **Data Handling**
   - Extracted header and data from the HDUs.
   - Saved data to a dummy FITS file with an additional dummy extension.

3. **Image Scaling**
   - Applied multiple scaling techniques:
     - **MinMax Scaling**
     - **Log Scaling**
     - **Z-Scaling** (produced the best visual clarity)
   - Used histograms to visualize the change from continuous to discrete pixel values.

4. **Filtering and Smoothing**
   - Compared **Gaussian smoothing** and a **normal filter**.
   - Analyzed their effects on z-scaled images and corresponding histograms.

5. **Feature Enhancement**
   - Applied **Meijering** and **Sato** filters on the z-scaled Gaussian images.
   - Visualized results using diverse color maps:
     - `gray`, `jet`, `hot`, `prism`, `nipyspectral`
   - Explored the **Corner_Foerstner** filter for feature detection.

---

## Observations & Learnings

- **Z-Scaling** effectively enhanced contrast and detail visibility.
- **Gaussian smoothing** reduced noise and improved clarity before filtering.
- **Different filters** (Meijering, Sato) reveal distinct structural features — choice depends on scientific intent.
- **Color maps** drastically change perception; while some outputs were mainly aesthetic, they aid in pattern recognition.
- **Corner Foerstner** outputs were visually interesting but require deeper understanding to extract meaningful data.

---

## Tools & Libraries
- `astroquery`
- `matplotlib`
- `astropy.io.fits`
- `scipy.ndimage`
- `skimage.filters`
- `numpy`

---

## Conclusion
This project deepened my understanding of astronomical image processing — from fetching real sky survey data to applying transformations and filters.  
It demonstrated how scaling, smoothing, and color mapping can transform raw telescope data into meaningful visual insights (or at least, beautiful cosmic art).

---


## Author
**Advika Tijare** ✨  
_Student exploring the universe, one pixel at a time._
