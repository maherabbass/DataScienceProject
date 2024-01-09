CMPS 262 – Data Science 
Sunday December 3, 2023
Maher Abbass – Joseph Yazbeck

Corruption and complexity: a scientific framework for the analysis of corruption networks


PART 1:
I.	Paper Overview:
The document titled "Corruption and Complexity: A Scientific Framework for the Analysis of Corruption Networks" by Issa Luna-Pla and José R. Nicolás-Carlock, published in Applied Network Science (2020), provides an in-depth analysis of corruption using the concepts and tools of complexity science, particularly network science. It aims to model corruption in a new light, beyond traditional methods, by focusing on a major corruption scandal in Mexico involving hundreds of shell companies used for embezzlement.

Key Points of the Study:
1. Approach and Objective: The study applies complex systems science and network theory to analyze corruption. It seeks to provide systematic evidence on corporate characteristics indicative of corruption, challenging traditional reductionist analyses.

2. Case Study: The document focuses on the corruption scandal involving the former governor of Veracruz, Mexico, Javier Duarte. This case involved a network of shell companies used to embezzle billions of dollars intended for social programs.

3. Data and Methodology: Data from 354 companies and 356 associated individuals were used, obtained from official sources and investigative journalism. The network analysis involved various metrics like density, diameter, average path length, and clustering coefficient.

4. Findings: 
   - Structural and Dynamic Analysis: The research showed that corruption networks have low density and average degree, indicating that not all companies connect with all people. The diameter and average path length metrics highlighted the extent of connected companies and people in the network.
   - Role of Personnel: The study emphasized the importance of company personnel in understanding corruption networks, noting that multiple roles played by individuals in different companies can reveal complex structures and behaviors.
   - Temporal Decomposition: Analysis by the year of company creation revealed that the network emerged from a self-organization process, with distinct characteristics each year.

5. Datasets Used:
- Source: The data was gathered from official sources accessible under Mexico's General Law of Transparency and Access to Information, by the NGO Mexicanos Contra la Corrupción e Impunidad and investigative journalists from Animal Político.
- Content: The dataset contained information about 354 companies and 356 people, including details about legal representatives, shareholders, administrators, and notaries, while keeping personal and company identities anonymous.

6. Conclusion:
- The study concludes that corruption is not only a complex phenomenon occurring within socio-political systems but can itself give rise to complex systems characterized by self-organizing and emergent phenomena.
- The use of complexity science and network theory in corruption studies can lead to better understanding and control mechanisms, potentially improving legal and administrative responses to corruption. 
This approach marks a significant shift from traditional corruption studies, emphasizing the need for an interdisciplinary and empirical methodology to effectively address the complexities of corruption.

7. Methods used in the Study:
In the study presented in the document, the authors utilized an empirical approach that incorporated concepts and tools from complex systems science, particularly network science. Here's a brief overview of the methods used:
a. Complex Systems Science: This method provides a comprehensive framework for studying natural and social adaptive systems. Complex systems science is instrumental in understanding systems that are characterized by multiple interacting components, which can produce emergent behavior that is not easily predictable from the properties of individual elements.
b. Network Science: A key component of complex systems science, network science was used to model and describe corruption scenarios. Network science focuses on the study of networks (e.g., social, biological, technological) and is particularly useful in understanding how relationships between entities (in this case, companies, and individuals) form structures and patterns that can influence behavior and outcomes.
c. Empirical Approach: The study employed an empirical approach to describe and model corruption. This involved collecting and analyzing real-world data to understand the dynamics of corruption networks.
d. Case Study of a Major Corruption Scandal: The research focused on a significant corruption scandal in Veracruz, Mexico, which involved a complex network of hundreds of shell companies used for embezzling funds intended for social programs. This case provided a practical application of complex systems and network science theories to analyze a real-world corruption network.
These methods allowed the researchers to move beyond traditional approaches to studying corruption, offering a multidimensional view of how corruption networks form, operate, and can be potentially dismantled or controlled.

Part 2:
II.	Working on Our Dataset:
We worked with a hypothetical dataset (AI generated) designed to represent corruption-related transactions and relationships between various entities. This dataset is not based on real-world data but constructed to simulate a network of interactions that could occur within a corruption scandal. 
Here's an overview of the dataset and its attributes:
1.	Dataset Attributes:
•	SourceID: The unique identifier for the entity initiating the transaction or relationship.
•	TargetID: The unique identifier for the entity receiving the transaction or relationship.
•	RelationshipType: The nature of the relationship, such as bribery, embezzlement, fraud, or nepotism.
•	TransactionAmount: The monetary value associated with the transaction. Missing values in this column were imputed using a conditional median approach based on the RelationshipType.
•	TransactionDate: The date on which the transaction or relationship was recorded. This could be used for temporal analysis to understand how the network changes over time.
•	SourceType: The role or position of the source entity, such as official, CEO, manager, or clerk.
•	SourceSector: The sector in which the source entity operates, like government, healthcare, construction, or finance.

PART 3: 
2.	Applying the Applications on our Dataset:
We applied the methods that were introduced in the paper (listed above), here is a summary of was done:

1. Complex Systems Science:
This part of the analysis involved creating a network graph from the dataset and calculating basic network metrics. The metrics provide an overview of the network's structure.

Results:
•	Number of Nodes (4351): Indicates a large number of entities are involved.
•	Number of Edges (4998): Suggests that there are many interactions between these entities.
•	Average Degree (2.2974): On average, each entity interacts with just over two other entities.
•	Network Density (0.000528): The network is sparse, meaning that not all entities are interconnected; there are likely isolated clusters within the network.
•	Average Clustering Coefficient (0.000421): Entities tend not to cluster together, which might indicate that corrupt activities are dispersed across the network rather than concentrated in tight groups.

2. Network Science:
This part focused on identifying the most influential entities and community structures within the network.

•	Degree Centrality: Calculated to identify influential entities based on the number of direct connections they have.
•	Community Detection: Implemented using the label propagation algorithm to identify communities within the network. Different communities might represent different types of corrupt activities or sectors.
•	Visualization: The network was visualized with nodes colored according to their community. This visual representation helps in understanding the community structure at a glance.

3. Empirical Approach:
This part analyzed the dataset using statistical methods to gain insights into the corruption activities recorded.

•	Descriptive Statistics: Provided a summary of the TransactionAmount data, showing a wide range of transaction values with a mean of around 48,661 and a notable standard deviation, indicating variability in the amount of money involved in different transactions.
•	Frequency Analysis: Revealed the counts of different types of relationships, sectors, and roles, indicating which types of corruption are most common and which sectors and roles are most involved.
•	Temporal Analysis: Showed the trend of transactions over time. The visualization suggests that the number of transactions fluctuates over time, which could indicate changes in corrupt activity levels, possibly as a result of external events or changes in policy.
              
              4. Case Study: 
To conduct a case study like the Veracruz corruption scandal using the dataset we have, we would approach it by focusing on specific features that are indicative of such a network of shell companies and embezzlement. 
Here's how we can proceed with the dataset we are working on:
•	Identify High-Value Transactions: By setting a high-value threshold, the application attempts to filter out transactions that are unusually large, which could be indicative of corrupt activities like embezzlement or money laundering.

•	Focus on Relevant Sectors: The application specifically looks at sectors where embezzlement is more likely to occur or where it would have a significant impact, such as social programs, non-profits, and government sectors.

•	Construct a Network for Analysis: By creating a graph from these transactions, the application sets the stage for network analysis, which can reveal how entities are interconnected, potentially identifying networks of shell companies used for embezzlement.

•	Detect Communities: Through community detection algorithms, we aim to find clusters within the network, which might represent groups of entities collaborating in corrupt activities.

•	Conduct Temporal Analysis: By grouping transactions by month and summing their amounts, the aim is to uncover temporal trends in the data, such as spikes in activity that could correspond to periods of intense corrupt activity or external events that may influence the frequency and size of transactions.

•	Visualize Trends Over Time: The visualization provides a clear graphical representation of the data, making it easier to spot trends, anomalies, or patterns that might merit further investigation.

In essence, the application serves to apply data science techniques to our corruption-related dataset to uncover potential signs of corruption, map out the relationships between entities involved, and understand the dynamics of the network over time. It's an exploratory step to identify areas for more detailed scrutiny, hypothesis formation, and eventually, to guide policy or investigative action.

PART 4:
3.Evaluation & Interpretation:

Based on the provided applications that we implemented on our hypothetical dataset, their outputs, and visualizations, we can derive the following implementation:

1.	Complex Science System Application Interpretation:
The network created from the dataset is sizable, with 4,351 nodes and 4,998 edges, indicating a substantial number of entities and interactions. The average degree is approximately 2.3, which means that on average, each entity is connected to around two other entities. The very low network density (about 0.00053) suggests that the network is quite sparse, with many potential connections not present. A similarly low average clustering coefficient (about 0.00042) indicates that tight-knit clusters within the network are rare, and there's not a strong tendency for nodes to form cliques.

The visualization of a subset of the network with 100 nodes was intended to give a manageable view of the network's structure. It would typically show how entities are interconnected and identify any patterns or hubs within this subset. However, it would not represent the entire network's complexity.

2.	Network Science System Application Interpretation:
Using network science principles, we calculated the degree centrality for all nodes, helping to identify which entities are most central within the network. Community detection, carried out with the label propagation algorithm, was visualized to reveal the community structures within the network. Different colors in the visualization indicate various communities or groups of nodes that are more densely connected to each other than to the rest of the network. These could represent entities that frequently engage in transactions with one another, possibly indicating collusion or concerted corrupt activities.

3.	Empirical Approach Application Interpretation:
The empirical analysis offered quantitative insights into the nature of transactions within the network. Transaction statistics show a wide range of values, from as low as 1,010 to as high as 99,994, with a mean transaction amount of around 48,661. This variability suggests that while some transactions are relatively small, others involve substantial sums, which could be indicative of major corrupt dealings or the involvement of higher-value targets within the network.

The frequency analysis revealed the most common types of relationships, with bribery being the most frequent, followed closely by nepotism, embezzlement, and fraud. The most involved sectors were finance and healthcare, which might suggest these areas are particularly susceptible to corruption within the network. The role distribution indicates that officials and managers are the most commonly involved in the transactions, which may reflect their positions of power and access to resources.

Looking at the bar chart that illustrates transaction trends over time, we can see that the occurrences of transactions in our dataset are fairly consistent, indicating a stable pattern of corrupt activity. The spikes in the data suggest episodes of heightened corruption, which could be tied to specific events or circumstances that we would need to investigate further to understand their causes.

From our perspective, the persistence of these activities, as shown by the lack of a declining trend, suggests that any anti-corruption measures in place during this period may not have been fully effective. This tells us that our analysis could potentially offer insights into how to better design and implement anti-corruption strategies. The data prompts us to consider external influences and internal policy changes that could affect the network's behavior. 

4.	Case Study Interpretation:
The bar chart titled "High-Value Suspect Transactions Over Time" presents the aggregated sum of suspect transaction amounts on a monthly basis. 
From the chart, we observe the following:

•	Consistent Activity: There is a consistent pattern of high-value transactions occurring throughout the time period. This suggests that the network's activity is not isolated to a specific timeframe but is spread consistently over the years.

•	Fluctuations: The bar chart shows fluctuations in the total amount of transactions, with certain months experiencing higher volumes. These spikes could be indicative of periods of increased corrupt activity or simply reflect the normal flow of transactions within the sectors under investigation.

•	No Clear Trend: There does not appear to be a clear increasing or decreasing trend in the transaction volumes over the years, which might suggest that the level of activity is relatively stable, or that anti-corruption measures have not significantly impacted the flow of transactions.

•	Potential Anomalies: Some months show particularly high volumes of transactions. These anomalies may warrant a closer look to understand the context and reasons behind these peaks, which could provide insights into specific events or practices contributing to these surges.
Given the pattern observed, further investigation is needed to contextualize these fluctuations. For instance, correlating the spikes with known political or economic events might reveal potential triggers for corrupt activity. Additionally, understanding the nature of the transactions and the entities involved during peak months could shed light on potential mechanisms of corruption within the dataset.

Interpretation of Results:
The analysis paints a picture of a spreading corruption network with periodic, yet possibly significant, corrupt interactions. The lack of dense clusters suggests a network where corrupt activities are not systemic or widespread among all entities but may be concentrated among certain groups or individuals. The presence of high-value transactions and the involvement of certain sectors and roles point to areas where anti-corruption efforts could be most effectively concentrated. The variability in transaction frequency over time could indicate that the network's activity is influenced by external factors, and these periods could be key targets for further investigation or intervention.

Conclusion:
In summary, the paper demonstrates that applying complex systems science and network theory to corruption analysis offers valuable insights into the structure and dynamics of corruption networks. It reveals that corruption is not merely a collection of isolated incidents but a sophisticated and adaptive system with emergent properties. The methodologies used provide a novel lens to identify patterns of corrupt behavior and the roles of various actors within these networks. The study concludes that this scientific framework is crucial for developing more effective and nuanced anti-corruption strategies, and it advocates for an empirical, data-driven approach to understanding and combating corruption.



