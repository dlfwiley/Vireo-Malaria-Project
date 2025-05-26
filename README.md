# Vireo-Malaria-Project
Title: Haemosporidian diversity dramatically differs among closely related, highly susceptible songbird species; Daniele L. F. Wiley, Jessie L. Williamson, Silas E. Fischer, Selina M. Bauernfeind, Henry Streby, Christopher C. Witt, and Lisa N. Barrow; project data and code.

Wiley et al., 2025 (in prep) Abundance and diversity of haemosporidian parasites dramatically differ among closely related vireo species.

In this study, we use pectoral tissues and whole blood samples of three closely related, elevational replacement species of vireo to characterize infection dynamics of avian Haemosporidians across their summer breeding sites in the American Southwest. We asked: What is the distribution, prevalence, and pathogen loads (parasitemia) experienced across these closely related species (Bell’s vireo: n = 20, gray vireo: n = 170, and plumbeous vireo: n = 58) during their breeding season in the southwestern U.S.? And what factors (i.e. host traits: species; environmental factors: temperature, precipitation; geographic features: latitude, elevation) are correlate with infection status and parasitemia?

Data are archived on FigShare: https://doi.org/10.6084/m9.figshare.28585943

DATASET All birds were sampled during summer months (May–August) spanning the years 1995–2019 across 27 unique sites in New Mexico and a single site in Utah, under appropriate federal, state, and local permits. Majority of samples were accompanied by vouchered specimens that were archived at the Museum of Southwestern Biology (MSB), University of New Mexico (UNM), except in the case of gray vireos that were released after sample collection. Samples used in this study represent 248 wild birds of three closely related vireo species (Bell’s vireo: n = 20, gray vireo: n = 170, and plumbeous vireo: n = 58). We screened samples via nested PCR amplification of the cytochrome b region for Haemoproteus and Plasmodium parasites and positive infections were quantified via microscopy following the protocol described in Valkiūnas (2005). Parasitemia represents the % of parasites counted across 10,000 red blood cells screened.

We identified and compared haplotypes to published records stored in the public databases GenBank (National Center for Biotechnology Information, US National Library of Medicine) and MalAvi (Bensch et al., 2009). Haplotypes that differed by one or more base pairs (~0.2% sequence divergence) from published sequences on GenBank or MalAvi were considered novel and named following MalAvi conventions. All sequences are uploaded to GenBank and MalAvi under [Accession Number #####] & [Accession Number #####].

Additionally, we documented aspects of sampling locality (i.e. latitude, longitude, elevation), and environmental factors known to impact pathogen prevalence and distribution (i.e. WORLDCLIM 19 bioclimatic variables to do with temperature and precipitation).

Analysis code is available on GitHub: https://github.com/dlfwiley/Vireo-Malaria-Project. Majority of data, except in the case of gray vireos released after sample collection, are linked to vouchered host and parasite specimens, housed at the Museum of Southwestern Biology (MSB) at the University of New Mexico, USA. Specimen records are accessible in the Artcos database (https://arctos.database.museum/).

R SCRIPTS

Host_Sample_Dataset.csv: This dataframe is the primary mastersheet used in all scripts below.

Host_Sample_Dataset_Metadata.xlsx: This spreadsheet defines each column (variable) in our project's mastersheet, with links to more information.

VirMal_statistical_analyses_pt1_infection-status.qmd: This script includes code meant for processing and assessing pathogen prevalence (response variable 1). It includes code for processing raw data, transforming variables, evaluating and eliminating outliers, and statistically assessing one-way relationships between prevalence and other variables (i.e. chi-squared, difference in means, logistic regressions, confidence intervals, and effect sizes). Start here.

VirMal_statistical_analyses_pt2_infection-status.qmd: This script includes code meant for processing and assessing pathogen infection parasitemia (response variable 2). It includes code for processing raw data, transforming variables, evaluating and eliminating outliers, and statistically assessing one-way relationships between intensity and other variables (i.e. difference in means, linear regressions).

VirMal_Bioclimatic_variables_PCA.qmd: This script covers the reduction of 19 WorldClim 2.1 (Fick & Hijmans, 2017) at 30 seconds (~1 km²) resolution into two principal component analyses. The first covering temperature-related variables and the second covering precipitation. It includes code to assess variable loadings and loading contributions which are what is reported in Supplemental Table S4-S5.

VirMal_Rarefaction.qmd: This script covers the use of the iNEXT R package (version 3.0.1; Chao et al., 2014; Hsieh et al., 2024) to estimate parasite lineage diversity and evaluate sampling completeness for host species with adequate data (gray and plumbeous vireos). Data input for haplotype abundance counts across hosts can be found in Table S3.

Questions? Contact me at dlfwiley [at] gmail.com.
