- # Project structure documentation

#### In this project documentation file, we will discuss the project folder structure and the placement of each project element in its place.

As you can see, the overall structure contains 5 main folders: data, docs, notebooks, reports, and sourcecode. Explanations about them are provided below.

- **data** ⇒ All data used in the project is placed in this folder.
  - **external** ⇒ Data imported from outside the project is stored in this folder.
  - **interim ** ⇒ Frequently used groupings and joins are processed once and stored in this section to avoid repeated processing.
  - **processed** ⇒ Cleaned and sorted data that is ready for statistical analysis is stored in this section.
  - **raw** ⇒ The raw project data is located in this folder.
- **docs** ⇒ Project related documents are located in this section.
- **notebooks** ⇒ The ipynb files are placed in this folder.
- **reports** ⇒ The reports and outputs of our statistical analyses are included in this section.
  - **figures** ⇒ The graphs drawn in the analysis are saved in this folder.
- **sourcecode** ⇒ The project source codes, such as data cleaning codes, will be placed in this section.
--
### Phase 1 – Clean Version (Simplified Mermaid Flowchart)


- A["📂 Parquet Files (day_1 ... day_n)"] ⇒ B["Load all daily files using pandas.read_parquet()"]
- B ⇒ C["Concatenate files by table (pd.concat)"]
- C ⇒ D["Merge all full tables on match_id"]
- D ⇒ E["Clean data (remove nulls, fix dtypes, create new columns)"]
- E ⇒ F["Save as tennis_master_clean.parquet"]
- F ⇒ G["Document columns in README.md"]

  **subgraph Tables Used**
    > T1["MatchEventInfo"]
    > T2["MatchHomeTeamInfo"]
    > T3["MatchAwayTeamInfo"]
    > T4["MatchTournamentInfo"]
    > T5["MatchTimeInfo"]
    > T6["MatchHomeScoreInfo"]
    > T7["MatchAwayScoreInfo"]
  end
  
  **style**
    > style Tables Used fill:#E6F3FF,stroke:#339,stroke-width:1px
    > style A fill:#F8F8FF,stroke:#888,stroke-width:1px
    > style D fill:#E8FFF0,stroke:#0A0,stroke-width:1px
    > style E fill:#FFF7E6,stroke:#AA6600,stroke-width:1px
    > style F fill:#FFF0F0,stroke:#C00,stroke-width:1px





