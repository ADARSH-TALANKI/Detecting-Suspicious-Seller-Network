Detecting Suspicious Seller Network
Overview:
This project focuses on identifying suspicious seller behavior using scraped data, feature engineering, and network-based analysis. The main idea behind this work was not just to write code, but to understand how a real-world objective can be achieved using a combination of manual coding and modern data analysis tools.
Instead of relying on a single approach, this project explores different methods at each stage (scraping, preprocessing, flag creation, visualization) and compares their effectiveness and limitations.

Motivation
In real investigations and data-driven analysis, problems are rarely solved using only code or only tools. Modern workflows often combine both.
The goal of this project was to simulate such a workflow and understand:
when coding gives more control and flexibility
when tools are faster and more convenient
where tools fall short and manual logic becomes necessary

Project Workflow
1. Data Collection
Seller data was obtained through web scraping.
BeautifulSoup was used to implement and understand manual scraping logic.
Octoparse was explored as a no-code alternative for automated scraping.
This helped in comparing the flexibility of code-based scraping with the convenience of tool-based solutions.

2. Data Cleaning and Preprocessing
After scraping, the dataset was cleaned and prepared for analysis.
Basic preprocessing steps such as handling missing values and formatting fields were performed before feature creation.

3. Feature Flag Engineering
To detect suspicious behavior, multiple flags were created based on seller activity patterns.

Two approaches were explored:
Manual flag creation using Python, which allowed full control over logic
OpenRefine, which was effective for transformations and grouping but limited for complex conditional rules
Due to these limitations, several important flags were implemented manually using code.

4. Manual Risk Scoring
Each flag was analyzed and assigned a relative risk weight based on its importance.
A final risk score was calculated by combining these weighted flags, and a threshold was chosen to flag potentially suspicious sellers.
This approach ensured transparency and interpretability of the results.

5. Network Visualization
To analyze relationships between sellers, the processed data was converted into a network format.
A .gexf file was generated and visualized using Gephi, which provided better insights into:
connections between entities
clusters and highly connected nodes

6. OSINT Exploration
Beyond the dataset, the project explored how flagged entities could be further investigated using OSINT tools such as Maltego.
This step demonstrates how analytical results can be extended into real-world investigation workflows.

Machine Learning Extension
As part of the overall team project, an unsupervised learning approach using Isolation Forest was implemented by another team member to validate suspicious behavior without relying on manually defined thresholds. This implementation is referenced conceptually but is not included in this repository.

Tools and Technologies Used
Python (Pandas, NumPy, NetworkX)
BeautifulSoup
Octoparse (explored)
OpenRefine (explored)
Gephi
Maltego
Jupyter Notebook

Key Takeaway

The key learning from this project is that effective analysis is not only about writing code, but also about choosing the right tools at the right stage and understanding their limitations. A hybrid approach combining coding, visualization tools, and OSINT techniques leads to more practical and realistic analytical workflows.
