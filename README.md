# EDA-Exercise-Regional-Resilience Brief
**Research Brief:**
UK Regional Resilience Audit – Quantifying Decoupling Between Economic Growth and Public Well-being

**Executive Summary:**
This brief presents key findings from an audit into UK regional resilience, specifically investigating the structural decoupling between economic growth and public well-being. Utilising unique metrics derived from Office for National Statistics (ONS) data and BBC regional news sentiment, the analysis reveals that while economic prosperity is evident, its translation into improved public satisfaction is highly uneven across the UK. Notably, London, despite its immense economic output, exhibits the highest '_Friction Score_', indicating a significant disconnect. This audit underscores that achieving the UK's 2030 growth targets requires a multi-dimensional policy approach that integrates well-being metrics alongside traditional economic indicators to foster genuine and equitable regional resilience.

**Introduction and Background:**
Achieving the government's aim for the UK to sustain G7 growth leadership by 2030 underscores a robust understanding of regional economic dynamics. Traditional economic metrics, such as Gross Value Added (GVA), often obscure critical localised pressures, institutional friction, and infrastructure limitations that prevent economic prosperity from translating into improved standards of living. 
This audit moves beyond such conventional measures to investigate the concept of '_adaptive regional resilience_'. This references a regions ability to maintain or reconfigure its socio-economic structures in response to shocks and, ultimately, to effectively absorb and translate economic gains into public well-being. The background literature highlights the importance of a region's '_absorptive capacity_'. Here, insufficient skilled labour or infrastructure can lead to '_extractive growth_', where economic influxes yield diminished returns for local welfare.

**Methodology:**
This analysis integrates diverse data sources to provide a comprehensive view of regional resilience, the study integrates:
i) Economic Data: Longitudinal GVA, population statistics, and GVA per head data were sourced from the Office for National Statistics (ONS) and processed into Polars DataFrames. This dataset provides a balanced panel spanning 18 years across UK geographical classifications (ITL1 and ITL2).
ii) Sentiment Data: Real-time regional news sentiment was acquired by web scraping headlines from an expanded set of BBC regional RSS feeds. Natural Language Processing (NLP) with TextBlob was used to assign polarity scores (-1 to 1) to these headlines, acting as a proxy for public perception and well-being.

Looking at the two sources above, two novel metrics were developed to quantify the relationship between economic activity and well-being:
i) Prosperity_Delta: Calculated as (GVA_Growth_Rate - Population_Growth_Rate), this _metric offers a refined measure of per-capita economic gain_, calculating whether economic expansion genuinely outpaces demographic growth.
ii) Friction_Score: Derived as (GVA_per_Head / |Sentiment_Score|), this crucial metric quantifies the structural decoupling. A higher Friction_Score indicates a greater disconnect between a region's economic output and its perceived well-being, signaling areas where economic gains may be diluted by infrastructure/insititutional failure.

**Key Findings:**
Prosperity_Delta :On average, understanding per capita economic gain, GVA growth slightly outpaced population growth across UK regions (mean = 0.02435), suggesting an overall trend toward increasing per-capita prosperity. However, this trend masks significant heterogeneity, with a wide range from -6.38% (where population growth significantly outstripped GVA growth) to 13.67% (indicating robust per-capita economic gains). This highlights varied success in translating overall economic growth into individual-level prosperity across regions.

Friction_Score: The Friction_Score proved to be a powerful indicator of structural decoupling. Descriptive statistics revealed an average Friction_Score of approximately 2.2 million, but with an exceptionally high standard deviation (10.7 million) and a maximum value reaching 211 million. This confirms that the problem of decoupling is not uniformly distributed but is acutely concentrated in certain outlier regions, where economic output is vastly disproportionate to public sentiment.

Identification of Decoupling Hotspots (Visualisations): The bar chart clearly identified specific Local Authorities with exceptionally high Friction_Scores. These regions are prime examples of the core problem, demonstrating areas where economic activity, despite its magnitude, is failing to translate into a corresponding positive public sentiment. The chart visually reinforces the notion of concentrated decoupling, highlighting the 'problem areas' for targeted policy.
The bivariate scatter map reinforced London's unique position. While exhibiting immense economic productivity (Avg_GVA_per_Head represented by bright color) and robust population growth (Avg_Population_Growth_Rate represented by large size), London also registered the highest Friction_Score. This suggests that despite its economic dynamism, factors such as high cost of living, infrastructure strain, or other socio-economic pressures are significantly impacting public sentiment, leading to a profound structural decoupling. 

**Implications and Policy Considerations:**
The findings demonstrate that while economic prosperity is present across UK regions, its translation into improved well-being is highly uneven. The Friction_Score acts as a crucial indicator of a region's adaptive resilience and absorptive capacity. A high score suggests that despite economic inputs, there's a struggle in translating these into perceived well-being, implying lower absorptive capacity or significant institutional/infrastructural constraints. 

This may point to several critical policy considerations:
i) Holistic Development Strategies: Policies focused solely on economic growth (e.g., GVA targets) may be insufficient. Regional development strategies must adopt a holistic view, integrating well-being metrics and sentiment analysis to ensure growth benefits local populations.
ii) Targeted Interventions: Regions identified with high Friction_Scores require multi-dimensional policy interventions that go beyond traditional economic stimuli. These interventions should address the underlying causes of disconnect, such as inadequate social or physical infrastructure, skills mismatches or governance issues, which impact public sentiment.
iii) Enhance Absorptive Capacity: Strategies must focus on building regional '_absorptive capacity'_ by investing in human capital (e.g., education, skills training, local institutional strength, and digital/physical infrastructure). This ensures that economic investments lead to sustainable improvements in local welfare and reduce '_friction_'.
iv) Continuous Monitoring: The Prosperity_Delta and Friction_Score provide _quantifiable metrics_ for ongoing monitoring and evaluation of regional policies. Regular tracking can identify emerging decoupling trends and assess the effectiveness of interventions. 

This audit provides robust empirical evidence for identifying regions where economic growth is structurally decoupled from public sentiment, thereby indicating areas requiring targeted policy interventions to foster genuine regional resilience and well-being.
