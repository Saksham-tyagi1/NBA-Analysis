# 🏀 NBA Shot Clustering Analysis - README

## 📌 Project Overview
This project analyzes **NBA players and teams** based on their **shot distribution patterns** using **clustering techniques**. It aims to uncover trends in shooting efficiency, player tendencies, and team strategies to better understand **what contributes to winning basketball games**.

## 📂 Data Used
- **Encoded Shot Data**: Feature-engineered dataset with categorical encoding, shot clock status, clutch moments, and advanced shot metrics.
- **NBA Shot Data**: Contains shot attempts, locations, shot distances, shot success rates, and game context.
- **Merged Game Event Data**: Includes additional in-game statistics such as player movement, passing, and shot clock conditions.
- **Optimized Data Formats**: The dataset is stored in Parquet format for efficient processing and memory optimization.
- **Encoded Shot Data**: Feature-engineered dataset with categorical encoding, shot clock status, clutch moments, and advanced shot metrics.
- **NBA Shot Data**: Contains shot attempts, locations, shot distances, shot success rates, and game context.
- **NBA Shot Data**: Contains shot attempts, locations, shot distances, shot success rates, and game context.
- **Player Information**: Player names, positions, and shooting tendencies.
- **Team Standings (2023-24 Season)**: Used to compare team success rates with shot distribution patterns.

## 🏀 Clustering Methodology
### **1️⃣ Player Clusters** (Shot Style)
Players were grouped based on their **shot selection, efficiency, and tendencies**:
- **Efficient Scorers (Cluster 0)** – High FG%, balanced shot selection.
- **Volume Shooters (Cluster 1)** – Take a high number of shots but with lower efficiency.
- **Specialist Shooters (Cluster 2)** – Focus on specific shot types (e.g., 3-point shooters, paint finishers).

### **2️⃣ Team Clusters** (Playstyle & Success)
Teams were categorized based on the **proportion of each player type in their lineup**:
- **Championship Contenders (Cluster 0)** – Highest win % and shooting efficiency.
- **Playoff Hopefuls (Cluster 1)** – Mid-tier teams with inconsistent performance.
- **Struggling Teams (Cluster 2)** – Lowest win %, inefficient shot selection.

## 🔑 Key Findings
- **Winning teams prioritize efficient scorers**, while struggling teams over-rely on volume shooters.
- **Shooting efficiency correlates with success**, with Championship Contenders having the highest FG%.
- **Specialist Shooters contribute selectively** but do not define overall team success.

## ⚙️ Installation & Requirements
### **Feature Engineering Steps**
- One-hot encoding for categorical variables such as `SHOT_TYPE`, `BASIC_ZONE`, and `ZONE_NAME`.
- Frequency encoding for `ACTION_TYPE`.
- Shot clock status mapping into phases (Very Early, Early, Late, Very Late).
- Rolling averages for `EFG_PCT` and `SCOREMARGIN` to capture momentum.
- Standardization and power transformation to handle skewed numerical features.
### **Prerequisites**
Ensure you have the following Python libraries installed:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### **Running the Analysis**
1. **Load and preprocess the dataset**:
   - Merge multiple season chunk files into a single DataFrame.
   - Optimize data types to reduce memory usage.
   - Handle missing values with appropriate imputation strategies.
2. **Perform clustering algorithms** to identify player and team shot patterns.
3. **Analyze feature correlations** to validate shot efficiency impacts.
4. **Generate visual insights** with efficiency and shot distribution charts.
1. **Load the dataset** and apply feature engineering transformations.
2. **Perform clustering algorithms** to identify player and team shot patterns.
3. **Analyze feature correlations** to validate shot efficiency impacts.
4. **Generate visual insights** with efficiency and shot distribution charts.
1. **Load the dataset** and preprocess it.
2. **Run clustering algorithms** to identify player and team clusters.
3. **Analyze the relationships** between shot selection, efficiency, and team success.
4. **Visualize findings** with charts and tables.

## 📊 Future Work
- Integrating **defensive metrics** to see how defense impacts shooting efficiency.
- Analyzing **player movement and shot creation** to refine shot clustering.
- Expanding to **playoff performance** for a deeper postseason analysis.
- **Team-Specific Recommendations**: Tailoring strategies for teams based on player composition and efficiency metrics.

## 🏀 Team-Specific Recommendations
### **Championship Contenders (Team Cluster 0)**
✅ Strengths:
- Balanced mix of **Efficient Scorers & Specialist Shooters**.
- Strong shot selection & high FG%.

📌 **Recommendations:**
- Maintain **roster stability** and focus on **shot creation improvements**.
- Optimize **defensive shot contesting** to limit opponent efficiency.
- If over-reliant on **Volume Shooters**, reduce mid-range shots.

### **Playoff Hopefuls (Team Cluster 1)**
❌ Weaknesses:
- **Mid-level shooting efficiency** (needs improvement).
- Imbalanced roster (too many **Volume Shooters, not enough Efficient Scorers**).

📌 **Recommendations:**
- **Recruit more Efficient Scorers (Cluster 0)** to improve **shot selection**.
- Encourage **Specialist Shooters (Cluster 2) to take more open 3PTs**.
- Reduce reliance on **low-efficiency mid-range shots**.
- Optimize **shot clock usage** to avoid rushed late-game shots.

### **Struggling Teams (Team Cluster 2)**
❌ Weaknesses:
- **Over-reliance on Volume Shooters (Cluster 1)** → Poor shot selection.
- **Lowest shooting efficiency** in the league.

📌 **Recommendations:**
- **Sign or develop Efficient Scorers (Cluster 0)** to improve **shot efficiency**.
- **Encourage more 3PT shooting** from Specialist Shooters (Cluster 2).
- **Focus on playmaking & ball movement** to generate **better shot opportunities**.
- **Limit mid-range shots from Volume Shooters**.
- Integrating **defensive metrics** to see how defense impacts shooting efficiency.
- Analyzing **player movement and shot creation** to refine shot clustering.
- Expanding to **playoff performance** for a deeper postseason analysis.

🚀 **This project provides data-driven insights into NBA shot efficiency and team success—helping teams optimize player roles and strategies!**

