# Spatial Price Discrimination in Russian Grocery Retail

This repository contains the replication code for my undergraduate thesis **"Location-Based Price Discrimination in Russian Grocery Retail"** (HSE University, 2025). The thesis was awarded the **Laureate of the HSE Best Research Paper Competition 2025**.

## 📄 Abstract

The study investigates whether major Russian grocery chains adjust prices based on regional poverty levels. Using a novel panel dataset of over 5 million weekly price observations from five federal retailers across 28 regions (2021–2022), I test whether cross-regional price variation reflects differences in local competitive conditions rather than cost factors alone.

## 🔧 Methodology

- **Data processing:** Merging price data with regional socio-economic indicators (income, poverty, wages, retail density, fuel prices, car ownership)
- **Feature engineering:** Identification of socially important products via keyword-based classification (NLP approach)
- **Core analysis:** Fixed-effects regressions with product, retailer, and week fixed effects; standard errors clustered at the regional level
- **Robustness checks:** Alternative specifications, subsample analyses (excluding the largest retailer), Driscoll–Kraay standard errors

## 📊 Key Results

- In non-regulated product categories, prices are significantly lower in poorer regions — evidence of price discrimination favouring wealthier areas.
- For socially important goods, the effect is weaker, suggesting compensatory pricing strategies.
- Retailers exhibit heterogeneous strategies: some show a positive poverty–price relationship, others a negative one.
- Lower base prices in poor regions are offset by less frequent discounts, equalising the final consumer burden.

## 🗂️ Data

The raw data are **not included** in this repository due to size and licensing. They can be accessed here:

- [Yandex.Disk](https://disk.yandex.ru/d/-KSMQUN3Vf8htQ) (original dataset)
- [HSE thesis page](https://spb.hse.ru/ba/economics/students/diplomas/1048202003) (contains metadata)

To run the code, download the data and place it in the `data/` folder.

## 🚀 Running the Code

All scripts are written in R and should be run in the order listed above. Required packages:

```r
install.packages(c("tidyverse", "fixest", "kableExtra", "openxlsx", "car"))
