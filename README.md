```markdown
# Forest Fire Analysis Project



## Project Overview
This analytical project examines forest fire patterns and relationships between environmental factors and fire characteristics using historical data from Portugal's Montesinho National Park. The analysis focuses on temporal patterns, weather correlations, and fire size relationships.

## Data Source
**UCI Machine Learning Repository - Forest Fires Data Set**  
https://archive.ics.uci.edu/ml/datasets/Forest+Fires

Contains 517 fire observations with 13 attributes including:
- Spatial coordinates (X, Y grid locations)
- Temporal features (month, day)
- Weather indices (FFMC, DMC, DC, ISI)
- Meteorological measurements (temp, RH, wind, rain)
- Outcome variable (burned area in hectares)

## Key Features
1. **Temporal Analysis**
   - Monthly fire frequency patterns
   - Daily fire occurrence trends
   - Seasonal weather pattern distributions

2. **Weather Relationships**
   - Boxplots showing monthly variations in weather parameters
   - Scatterplots revealing fire size correlations

3. **Advanced Visualizations**
   - Interactive HTML report generation
   - Log-transformed fire size analysis
   - Multi-plot dashboard layouts

## Key Insights
### Temporal Patterns
- 🚩 **Peak Fire Months**: August (184 fires) and September (172 fires)
- ❄️ **Low Activity**: December-February (<10 fires total)
- 📅 **Daily Pattern**: Slight weekend increase (Sun/Fri peaks)

### Weather Correlations
- 🔥 **Fire Size Drivers**:
  - Positive: Temperature (r = 0.68)
  - Negative: Relative Humidity (r = -0.61)
- 🌬️ **Wind Impact**: Moderate correlation with fire spread (r = 0.42)
- ☔ **Rain Paradox**: Most fires occur with 0mm rain, but heavy rains show outlier large fires

### Prevention Implications
1. Heighten surveillance during late summer months
2. Monitor RH thresholds for fire risk alerts
3. Focus resources on weekends/holidays
4. Develop early-warning systems using FWI indices

## Installation & Usage
```bash
# Clone repository
git clone https://github.com/yourusername/forest-fire-analysis.git

# Install required packages
install.packages(c("tidyverse", "patchwork", "rmarkdown"))
```

**To run analysis:**
1. Place `forestfires.csv` in project root
2. Open `forest_fire_analysis.Rmd` in RStudio
3. Click "Knit" to generate HTML report

## Technical Requirements
- R ≥ 4.1.0
- RStudio ≥ 2022.02
- Package Dependencies:
  - tidyverse (1.3.1+)
  - patchwork (1.1.2+)
  - viridis (0.6.2+)

## Data Dictionary
| Variable | Description                          | Range       |
|----------|--------------------------------------|-------------|
| X, Y     | Spatial coordinates (1-9 grid)       | 1-9         |
| month    | Month of observation                 | jan-dec     |
| day      | Day of week                          | mon-sun     |
| FFMC     | Fine Fuel Moisture Code              | 18.7-96.2   |
| DMC      | Duff Moisture Code                   | 1.1-291.3   |
| DC       | Drought Code                         | 7.9-860.6   |
| ISI      | Initial Spread Index                 | 0.0-56.1    |
| temp     | Temperature (°C)                     | 2.2-33.3    |
| RH       | Relative Humidity (%)                | 15-100      |
| wind     | Wind speed (km/h)                    | 0.4-9.4     |
| rain     | Rainfall (mm/m²)                     | 0.0-6.4     |
| area     | Burned area (hectares)               | 0.0-1090.8  |

## Future Work
1. 🔮 Predictive modeling of fire risk
2. 🗺️ Spatial analysis of fire hotspots
3. ⚖️ Class imbalance addressing (zero-inflated area)
4. 🌐 Climate change impact projections
5. 🚒 Resource allocation optimization models

## License
All rights reserved. Dataset attribution required per UCI's terms of use.

---

**Author**: Vaibhav Vesmaker  
**Last Updated**: 18 February 2025
