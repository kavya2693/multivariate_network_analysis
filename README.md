# Multivariate and Network Analysis of Dry Bean Dataset
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/d870951b-5282-474a-8779-dea5d4a3d2a5)

## Overview

This repository hosts a comprehensive analysis of the Dry Bean dataset, leveraging advanced multivariate and network analysis techniques to unlock valuable insights into bean health and quality. In the agricultural sector, particularly in the context of legume production, understanding the nuances of bean characteristics can significantly enhance quality control, breeding programs, and overall yield optimization.

## Business Relevance

In the realm of agribusiness, the ability to predict and ensure bean quality before harvest is paramount. Our analysis provides stakeholders with a data-driven foundation to make informed decisions, ranging from cultivation strategies to market positioning. By identifying the key factors that determine bean health and employing network analysis, we offer a novel perspective on how different bean attributes interconnect and influence overall quality.

## Why Dry Bean Data Analysis?

Dry beans are a staple food source globally, known for their nutritional value. The quality of beans directly impacts their market value, consumer acceptance, and nutritional content. Therefore, understanding the intricate relationships between various bean attributes is crucial for stakeholders to enhance production quality, align with market demands, and ensure food security.
The dataset offers a unique vantage point into the agricultural domain, providing images of 13,611 grains across 7 different dry bean types. These images, captured with precision, have been analyzed to extract a total of 16 features per grain, encompassing 12 dimensional attributes and 4 shape descriptors.

## Dataset Characteristics

- **Nature of Data:** Multivariate, with a focus on both dimensional and shape attributes to provide a holistic view of bean characteristics.
- **Subject Area:** Biology, specifically botany and agricultural sciences, emphasizing the biological and physical attributes of dry beans.
- **Associated Tasks:** Primarily classification, aiming to distinguish between seven bean varieties based on their physical attributes.
- **Feature Types:** Includes both integer and real-number data types, reflecting the quantitative nature of the extracted features.
- **Instance Count:** The dataset comprises 13,611 instances, each representing a unique grain image analyzed.
- **Feature Count:** A total of 16 features have been extracted for each instance, offering a detailed perspective on the beans' physical attributes.

![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/99c47a43-c525-411e-a05e-649db464ffa4)

## Additional Dataset Information

This dataset was curated with an eye toward market dynamics, focusing on bean forms, shapes, types, and structures that are significant in commercial contexts. The underlying computer vision system was meticulously developed to differentiate among seven registered bean varieties, facilitating precise seed classification in line with market standards.


## Project Significance

- **Quality Assessment:** Our analysis assists in establishing a robust framework for assessing bean quality through various dimensions, including size, shape, and texture.
- **Predictive Insights:** By understanding the relationships between different bean attributes, producers can predict the quality of their yield, enabling proactive quality enhancement measures.
- **Decision Making:** The insights derived from this analysis empower stakeholders to make data-informed decisions regarding cultivation practices, storage, and distribution strategies to maximize quality and profitability.

## Key Variables and Analysis

We explore numerous variables capturing the physical characteristics of beans, which are crucial for determining their quality. These include dimensions like area, perimeter, major axis length, minor axis length, and several others, which collectively provide a multidimensional view of bean health.

Through network analysis, we illustrate the interdependencies among these variables, offering a comprehensive understanding of how various attributes correlate and impact bean quality.

## Technologies and Packages Used

- **R Programming:** Our analysis is conducted using R, a powerful tool for statistical computing and graphics.
- **`dplyr`:** For data manipulation and cleaning, providing a straightforward syntax for complex data operations.
- **`ggcorrplot`:** Utilized for visually representing correlation matrices, facilitating an intuitive understanding of the relationships among variables.
- **`igraph`:** Employed for creating network visualizations, illustrating the intricate connections between bean attributes.
Full code can be found in drybean.pynb and full report in drybean_report.md

## Conclusion

In conclusion, the analysis of the Dry Bean dataset provided a detailed examination of the intricate relationships between its variables, utilizing advanced multivariate and network analysis techniques. Initially, 344 significant correlations were identified, but after implementing statistical corrections to address the potential for false discoveries, this number was refined to 270. This reduction highlights the importance of statistical rigor in ensuring the reliability of the findings. The analysis not only sheds light on the complex interactions within the dataset but also establishes a foundation for future research. By accurately identifying and understanding these relationships, researchers can build upon this work with confidence, knowing that the insights gained are based on substantiated connections, thus enhancing the quality and impact of subsequent studies in the field.
