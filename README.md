<!-- Profile README — repo: mostafaelmehi/mostafaelmehi (upload banner.svg next to this file) -->

<div align="center">

<img src="./banner.svg" alt="Moustafa Elmehy — AI Engineer · NLP & LLMs · MLOps" width="100%"/>

<a href="https://www.linkedin.com/in/Moustafa-Elmehy"><img src="https://img.shields.io/badge/LinkedIn-Moustafa%20Elmehy-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:mostafa94955@gmail.com"><img src="https://img.shields.io/badge/Email-Get%20in%20touch-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<img src="https://komarev.com/ghpvc/?username=mostafaelmehi&style=for-the-badge&color=36BCF7&label=PROFILE+VIEWS"/>

<br/><br/>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=36BCF7&center=true&vCenter=true&width=720&lines=I+build+AI+applications+%E2%80%94+and+evaluate+them+honestly.;Fine-tuned+LLaMA+3.2+(QLoRA)+%E2%86%92+Macro-F1+0.70+vs+0.57;RAG+%C2%B7+AI+Agents+%C2%B7+n8n+%C2%B7+LangChain;From+notebook+to+API%3A+FastAPI+%C2%B7+MLflow+%C2%B7+Docker" alt="Typing SVG"/></a>

</div>

---

## 🧠 About me

```python
class MoustafaElmehy:
    role       = "AI Engineer · NLP & LLM applications"
    based_in   = "Dortmund, Germany 🇩🇪"
    education  = "B.Sc. Informatik (Data Science) @ FH Dortmund — 2026, thesis graded 1.5"
    work       = "Data Trust Analyst (working student) @ TELUS International — evaluating AI-generated output"
    focus      = ["LLM fine-tuning", "RAG & AI agents", "honest model evaluation", "MLOps"]
    principles = ["dedupe before you split", "no data leakage", "simple model first", "measure, don't guess"]
    speaks     = {"Arabic": "native", "German": "C1", "English": "B2"}
```

---

## 🛠️ Tech stack

<div align="center">

| | |
|:--|:--|
| **Languages** | <img src="https://skillicons.dev/icons?i=python,sql,r,java,mysql&theme=dark" height="40"/> |
| **ML & LLMs** | <img src="https://skillicons.dev/icons?i=pytorch,sklearn&theme=dark" height="40"/> <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" height="32"/> <img src="https://img.shields.io/badge/OpenAI%20API-412991?style=for-the-badge&logo=openai&logoColor=white" height="32"/> |
| **RAG & Agents** | <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" height="32"/> <img src="https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" height="32"/> <img src="https://img.shields.io/badge/Vector%20DBs-36BCF7?style=for-the-badge" height="32"/> |
| **MLOps & Cloud** | <img src="https://skillicons.dev/icons?i=fastapi,docker,githubactions,azure,aws,git&theme=dark" height="40"/> <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" height="32"/> |
| **Analytics** | <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" height="32"/> <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" height="32"/> <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" height="32"/> |

</div>

---

## 🚀 Featured work
> Click a project to expand it.

<details open>
<summary><b>🎓 From Bag-of-Words to Specialized LLMs</b> — IT support ticket classification <i>(Bachelor thesis · 2026)</i></summary>
<br/>

**Problem:** route support tickets automatically to one of **10 departments**, and find out whether a fine-tuned LLM really beats classical NLP.

**What I did**
- Cleaned **29,651** tickets → **25,222** after removing **4,428 exact duplicates** *before* splitting, so no ticket leaks from train into test
- Benchmarked 4 classical pipelines: Naive Bayes (BoW / TF-IDF), Logistic Regression (TF-IDF), Random Forest (Word2Vec)
- Fine-tuned **LLaMA 3.2 3B** with **QLoRA**, comparing staged vs. single-run training and LoRA ranks r ∈ {8, 16}

**Result**

```mermaid
xychart-beta
    title "Macro-F1 on the test set"
    x-axis ["Best classical (LogReg + TF-IDF)", "Fine-tuned LLaMA 3.2 3B"]
    y-axis "Macro-F1" 0 --> 1
    bar [0.57, 0.70]
```

The LLM wins on quality; Logistic Regression stays the pragmatic choice when compute is tight.

`PyTorch` `Hugging Face` `QLoRA` `scikit-learn` `NLP`
</details>

<details>
<summary><b>⚽ Expected Assists in pro football</b> — interpretable ML + MLOps pipeline</summary>
<br/>

**Question:** can a player's expected-assist value be explained from performance data?

- Player data from Europe's **top 5 leagues**; removed leakage-prone variables and players under 270 minutes
- Selected **33 of 260+ features** via Mutual Information + Sequential Forward Selection with cross-validation
- The simpler **linear model beat Random Forest** — **R² = 0.917** on test data; key drivers: key passes & passes into the box
- Wrapped as a service with **FastAPI**, experiment tracking in **MLflow**, packaged with **Docker**

`Python` `scikit-learn` `FastAPI` `MLflow` `Docker`
→ [**View repo**](https://github.com/mostafaelmehi/xa-expected)
</details>

<details>
<summary><b>🧩 Solving photographed crosswords with AI</b> — vision + LLM pipeline</summary>
<br/>

- Pipeline that aligns the photo, detects the grid and answer fields, and structures clues by direction and length
- **GPT via the OpenAI API** for text recognition and answer suggestions, plus an external reference source
- LLM answers **validated by rules** (word length + crossing letters), so only consistent answers make it into the solution

`Python` `OpenAI API` `Computer Vision` `LLM validation`
</details>

<details>
<summary><b>☕ Starbucks customer analysis</b> — CRISP-DM + Power BI</summary>
<br/>

- Full analysis notebook: survey cleaning, multi-answer encoding, customer segmentation, preferences & marketing channels
- Separate **Power BI dashboard** for purchase and satisfaction patterns
- Derived marketing and assortment recommendations to grow revenue and reduce food waste

`Python` `Pandas` `Power BI` `CRISP-DM`
→ [**View repo**](https://github.com/mostafaelmehi/starbucks-full-project)
</details>

<details>
<summary><b>🏀 More projects</b></summary>
<br/>

- [NBA player salaries](https://github.com/mostafaelmehi/ML-project-NBA-Player-Salaries-) — ML regression on player stats
- [Football analysis in R](https://github.com/mostafaelmehi/football-5th-sms) — statistical analysis
- [Data analysis lab](https://github.com/mostafaelmehi/praktikum2) — university data-analysis task
</details>

---

## 🔁 How I take a model from idea to production

```mermaid
flowchart LR
    A[📦 Data] --> B[🧹 Clean · dedupe · no leakage]
    B --> C[🧪 Baseline first]
    C --> D[🦙 Fine-tune / RAG]
    D --> E[📊 Evaluate & track · MLflow]
    E --> F[⚡ Serve · FastAPI]
    F --> G[🐳 Ship · Docker + CI/CD]
    G --> H[👀 Monitor]
    H -. feedback .-> A
```

---

## 📊 GitHub activity

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=mostafaelmehi&show_icons=true&theme=tokyonight&hide_border=true&count_private=true"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mostafaelmehi&layout=compact&theme=tokyonight&hide_border=true"/>

<img src="https://streak-stats.demolab.com?user=mostafaelmehi&theme=tokyonight&hide_border=true"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=mostafaelmehi&theme=tokyo-night&hide_border=true&area=true" width="100%"/>

</div>

---

<div align="center">

### 🤝 Open to AI Engineer, ML Engineer & AI Consultant roles

<i>"I don't just build models — I check whether they're actually better."</i>

<a href="https://www.linkedin.com/in/Moustafa-Elmehy"><img src="https://img.shields.io/badge/Let's%20connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>

</div>
