# Multivariate Analysis and Network Analysis

## Introduction
In this report, I delve into an in-depth analysis of the Dry Bean dataset, applying multivariate and network analysis techniques. The focus is to explore the relationships among variables through correlation and partial correlation analyses, visualize them, and assess the impact of statistical adjustments on the findings.

## Methodology
### Step 1: Exploratory Analysis
I initiated the analysis by loading the Dry Bean dataset and preparing it for analysis. This preparation involved selecting specific variables, excluding the 'Class' variable, and adding 34 randomly generated variables to the dataset. To explore the relationships among these variables, I computed the correlation matrix using R's cor() function. Given the singularity of the variance-covariance matrix, the correlation matrix was chosen as the basis for further analysis. For partial correlations, the consideration was to apply matrix operations and potentially utilize the ppcor package, which is tailored for such calculations.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/9596cc58-d575-40f1-9285-b2111db3302f)

### Step 2: Exploration of Correlations
The exploration aimed to discern the strength and nature of correlations within the dataset. The focus was on distinguishing between the correlations among the original variables and those involving the newly added random variables. Utilizing visualization tools such as ggcorrplot, thresholding techniques were applied to highlight significant correlations, setting less significant values to zero for a clearer visual representation.
Here, the examination was on the correlations within the original variables and between the original and random variables. The goal was to identify strong and weak correlations, assisting in understanding the dataset's structure.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/51bfb5ce-c12d-487a-9af4-9b1f5ae26742)
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/eef30535-3be0-453a-8e31-1a24f8c47346)

### Step 3: Pairwise Table of Correlations
To facilitate a more detailed analysis, a pairwise table of correlations was constructed. This table laid out each variable pair alongside their corresponding correlation and partial correlation values, providing a structured overview of the relationships within the dataset.
Here, the correlation information was converted into a pairwise table format. This table lists each pair of variables alongside their correlation and partial correlation values.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/9613e981-92cd-4aff-8d5c-87431031d044)

### Step 4: Significance Testing
The next step was to ascertain the statistical significance of the observed correlations. By applying z-tests on Fisher's transformation to the correlation values, it was identified which correlations were significant at the 0.05 level. This step was crucial in distinguishing meaningful relationships from those that might occur by chance.
Now, the determination of the statistical significance of the correlations using z-tests based on Fisher's transformation was made. This step helps identify meaningful relationships.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/2547c6dc-d5e1-4fff-b79f-4a0aa496d9a5)

### Step 5: Network Creation
With significant correlations identified, the igraph package was employed to create networks illustrating these relationships. This visual representation allowed the observation of the interconnectedness of variables within the dataset, highlighting the most prominent relationships.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/aaaaaeed-8fd2-4338-80f3-53e1cf461a41)
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/6ad5d5d8-5e6d-45da-ba1b-75be9e52e107)

Using significant correlations to build a network. Each node represents a variable, and edges indicate significant correlations.

### Step 6: Analysis of Discoveries
In this phase, the findings were categorized into true and false discoveries, based on whether the correlations involved the original variables or the added random variables. The False Discovery Rate (FDR) was calculated to quantify the extent of false discoveries, providing insight into the reliability of the findings.
The assessment was on the number of true and false discoveries in the network, which helped understand the data's structure and the potential for misleading findings.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/d7820c16-4948-4aa8-887f-c4e76d98e257)

### Step 7: P-value Adjustment and Network Re-evaluation
Finally, the p-values were adjusted using the Bonferroni and Benjamini-Hochberg methods to address the issue of multiple comparisons. This adjustment refined the network, reducing the number of spurious connections and enhancing the accuracy of the analysis. The network was then re-evaluated, and the FDR was recalculated, assessing the impact of these adjustments on the initial findings.
Adjusting p-values to control false discoveries and recreating the network using these adjusted values to more accurately reflect significant relationships.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/571cce69-fc2f-4336-8847-75f07970d57c)
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/e56f7847-9390-42ef-8637-84e03292278a)

### Step 8: Visualizing the changes in network structure
Here, the focus was on the changes in the number of significant correlations after adjustment and how this reflects on the network's structure.
![image](https://github.com/kavya2693/multivariate_network_analysis/assets/127579722/b77ed9c1-6b79-45a6-b37b-f7c5c90bb556)

## Summary:
Network Analysis:
Utilizing the igraph package, a network representation was constructed based on significant correlations, identified through z-tests on Fisher's transformation. Initially, the network showcased 344 significant correlations. However, upon adjusting the p-values using the Bonferroni method to mitigate the risk of false discoveries, the number of significant correlations was refined to 270.

## Insights:
- **Reduction in Significant Correlations:** The adjustment of p-values led to a decrease from 344 to 270 significant correlations, indicating a substantial impact of the adjustment process on the network's complexity.
- **Network Simplification:** The network's simplification post-adjustment underscores the importance of statistical rigor in distinguishing meaningful relationships from those that may arise due to chance.
- **Discovery Analysis:** The analysis reveals true discoveries (among the original variables) from false ones (involving the random variables), with the false discovery rate (FDR) being recalculated post-adjustment to reflect a more accurate picture of genuine associations.
- **Implications for Further Research:** The refined network, stripped of spurious correlations, provides a clearer, more reliable foundation for future analyses, enabling researchers to focus on relationships that are statistically validated.

## Conclusion:
The multivariate and network analysis of the Dry Bean dataset highlighted the intricate relationships among its variables. Through rigorous statistical methods, significant correlations were identified, adjusted for potential false discoveries, and the network of relationships was visualized, providing valuable insights into the dataset's structure. The findings underscore the importance of statistical adjustments in ensuring the validity and reliability of correlation analyses in complex datasets.
