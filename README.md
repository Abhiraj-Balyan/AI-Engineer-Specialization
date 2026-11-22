<div align="center">

# 🧠 AI Engineer Specialization

### Step-by-step notebooks, line-by-line code explanations, theory notes and projects across 13 courses

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?logo=jupyter&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-FF6F00?logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/Hugging%20Face-Transformers-FFD21E?logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-RAG-1C3C3C)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

## 📑 Table of Contents

1. [Overview](#-overview)
2. [Learning Path](#-learning-path)
3. [Repository Architecture](#-repository-architecture)
4. [Courses](#-courses)
5. [Concept Architecture Diagrams](#-concept-architecture-diagrams)
6. [Notebook Format](#-notebook-format)
7. [Tech Stack](#-tech-stack)
8. [Getting Started](#-getting-started)
9. [Workflow](#-workflow)
10. [Progress Tracker](#-progress-tracker)
11. [Skills Matrix](#-skills-matrix)
12. [Roadmap](#-roadmap)
13. [Contributing](#-contributing)
14. [License](#-license)
15. [Author](#-author)

---

## 🎯 Overview

This repository is a complete, hands-on record of the **AI Engineer specialization**: 13 courses, about **168 hours** of material, from classical machine learning to deep learning, transformers, LLM fine-tuning, RAG and AI agents.

Every topic is documented in the same detailed way:

- **Annotated Jupyter notebooks**: concept, code, and a line-by-line explanation of what each line does and why
- **Theory notes**: formulas, intuition and cheat sheets in plain markdown
- **Lab and project solutions**: graded work with write-ups
- **Reusable code**: clean `.py` modules extracted from the notebooks
- **Diagrams**: architecture and pipeline visuals for every major concept

### Goals

| Goal | How this repo delivers it |
|---|---|
| Deep understanding | Every line of code is explained, not just run |
| Reproducibility | Pinned dependencies, fixed seeds, relative paths |
| Portfolio quality | Clean structure, READMEs per course, real projects |
| Fast revision | Notes, cheat sheets and takeaways per notebook |

---

## 🗺 Learning Path

```mermaid
flowchart LR
    A["Foundations<br/>Python, NumPy, Pandas"] --> B["Course 01<br/>Machine Learning"]
    B --> C["Course 02<br/>Deep Learning with Keras"]
    C --> D["Course 03<br/>Keras and TensorFlow"]
    B --> E["Course 04<br/>Neural Networks and PyTorch"]
    E --> F["Course 05<br/>Deep Learning with PyTorch"]
    D --> G["Course 06<br/>AI Capstone"]
    F --> G
    G --> H["Course 07<br/>LLM Architecture and Data"]
    H --> I["Course 08<br/>Foundational NLP Models"]
    I --> J["Course 09<br/>Transformers"]
    J --> K["Course 10<br/>Fine-Tuning Transformers"]
    K --> L["Course 11<br/>Advanced LLM Fine-Tuning"]
    L --> M["Course 12<br/>AI Agents, RAG, LangChain"]
    M --> N["Course 13<br/>RAG Capstone Project"]

    classDef ml fill:#dbeafe,stroke:#3b82f6,color:#000;
    classDef dl fill:#fde68a,stroke:#f59e0b,color:#000;
    classDef genai fill:#dcfce7,stroke:#22c55e,color:#000;
    class B ml;
    class C,D,E,F,G dl;
    class H,I,J,K,L,M,N genai;
```

**Legend:** 🔵 Classical ML · 🟡 Deep Learning · 🟢 Generative AI and LLMs

---

## 🏗 Repository Architecture

### Folder structure

```
ai-engineer-specialization/
│
├── README.md                          # This file
├── LICENSE
├── requirements.txt                   # All Python dependencies
├── .gitignore
│
├── docs/                              # Repo-wide documentation
│   ├── NOTEBOOK_TEMPLATE.md           # Standard notebook format
│   ├── GIT_WORKFLOW.md                # Commit and branch conventions
│   └── GLOSSARY.md                    # Terms and definitions
│
├── shared/                            # Code and data shared by all courses
│   ├── utils/                         # Plotting, metrics, data loaders
│   └── datasets/                      # Small datasets, download scripts
│
├── 01-machine-learning-with-python/
├── 02-intro-deep-learning-keras/
├── 03-deep-learning-keras-tensorflow/
├── 04-intro-neural-networks-pytorch/
├── 05-deep-learning-pytorch/
├── 06-ai-capstone-deep-learning/
├── 07-genai-llm-architecture-data-prep/
├── 08-genai-foundational-models-nlp/
├── 09-genai-language-modeling-transformers/
├── 10-genai-engineering-finetuning-transformers/
├── 11-genai-advanced-finetuning-llms/
├── 12-ai-agents-rag-langchain/
└── 13-project-genai-rag-langchain/
```

### Inside every course folder

```
NN-course-name/
├── README.md        # Course overview, module checklist, key concepts
├── notebooks/       # Annotated Jupyter notebooks (one per topic, labs included)
├── notes/           # Theory notes in markdown
└── project/         # Graded assignments and final project
```

### How the pieces connect

```mermaid
flowchart TD
    subgraph Course["📁 Course Folder"]
        NB["notebooks/<br/>Annotated notebooks"]
        NOTES["notes/<br/>Theory notes"]
        PROJ["project/<br/>Graded work"]
    end

    subgraph Shared["📁 shared/"]
        UTILS["utils/<br/>Helper functions"]
        DATA["datasets/<br/>Small datasets"]
    end

    NB -->|"load data"| DATA
    PROJ -->|"load data"| DATA
    NB -->|"uses"| UTILS
    PROJ -->|"uses"| UTILS
    NOTES -.->|"theory behind"| NB
    NB -->|"skills applied in"| PROJ
```

---

## 📚 Courses

| # | Course | Hours | Focus | Folder |
|---|---|---|---|---|
| 01 | Machine Learning with Python: Build Real-World ML Models | 20 | Regression, classification, clustering, evaluation | [📂](01-machine-learning-with-python/) |
| 02 | Introduction to Deep Learning & Neural Networks with Keras | 10 | Perceptrons, backpropagation, first Keras models | [📂](02-intro-deep-learning-keras/) |
| 03 | Deep Learning with Keras and TensorFlow | 23 | CNNs, RNNs, autoencoders, transfer learning | [📂](03-deep-learning-keras-tensorflow/) |
| 04 | Introduction to Neural Networks and PyTorch | 19 | Tensors, autograd, training loops | [📂](04-intro-neural-networks-pytorch/) |
| 05 | Deep Learning with PyTorch | 21 | Deep networks, CNNs, regularization | [📂](05-deep-learning-pytorch/) |
| 06 | AI Capstone Project with Deep Learning | 15 | End-to-end deep learning project | [📂](06-ai-capstone-deep-learning/) |
| 07 | Generative AI and LLMs: Architecture and Data Preparation | 6 | Tokenization, embeddings, text data pipelines | [📂](07-genai-llm-architecture-data-prep/) |
| 08 | Gen AI Foundational Models for NLP & Language Understanding | 10 | Language models, NLP tasks | [📂](08-genai-foundational-models-nlp/) |
| 09 | Generative AI Language Modeling with Transformers | 9 | Attention, transformer blocks, GPT and BERT | [📂](09-genai-language-modeling-transformers/) |
| 10 | Generative AI Engineering and Fine-Tuning Transformers | 8 | Hugging Face, PEFT, LoRA | [📂](10-genai-engineering-finetuning-transformers/) |
| 11 | Generative AI Advanced Fine-Tuning for LLMs | 9 | Instruction tuning, RLHF, DPO | [📂](11-genai-advanced-finetuning-llms/) |
| 12 | Fundamentals of AI Agents Using RAG and LangChain | 9 | Embeddings, vector stores, RAG, agents | [📂](12-ai-agents-rag-langchain/) |
| 13 | Project: Generative AI Applications with RAG and LangChain | 9 | Full RAG application | [📂](13-project-genai-rag-langchain/) |

**Total: 168 hours**

### Course Breakdown by Category

```mermaid
pie showData
    title Hours by Category
    "Classical ML (01)" : 20
    "Deep Learning (02-06)" : 88
    "Generative AI and LLMs (07-11)" : 42
    "RAG and Agents (12-13)" : 18
```

---

## 🧩 Concept Architecture Diagrams

### 1. Machine Learning Pipeline (Course 01)

```mermaid
flowchart LR
    A["Raw Data<br/>CSV, SQL, API"] --> B["Data Cleaning<br/>missing values, outliers"]
    B --> C["Feature Engineering<br/>encoding, scaling"]
    C --> D["Train / Test Split"]
    D --> E["Model Training<br/>fit"]
    E --> F["Evaluation<br/>accuracy, R², F1"]
    F -->|"poor results"| G["Hyperparameter Tuning<br/>GridSearchCV"]
    G --> E
    F -->|"good results"| H["Final Model<br/>save and deploy"]
```

### 2. Neural Network Training Loop (Courses 02 to 05)

```mermaid
flowchart TD
    A["Input Batch"] --> B["Forward Pass<br/>layers and activations"]
    B --> C["Predictions"]
    C --> D["Loss Function<br/>MSE, Cross-Entropy"]
    D --> E["Backward Pass<br/>compute gradients"]
    E --> F["Optimizer Step<br/>SGD, Adam"]
    F --> G{"More batches<br/>or epochs?"}
    G -->|"yes"| A
    G -->|"no"| H["Trained Model"]
```

### 3. Feed-Forward Network Structure

```mermaid
flowchart LR
    subgraph Input["Input Layer"]
        I1(("x1"))
        I2(("x2"))
        I3(("x3"))
    end
    subgraph Hidden1["Hidden Layer 1"]
        H1(("h1"))
        H2(("h2"))
        H3(("h3"))
        H4(("h4"))
    end
    subgraph Hidden2["Hidden Layer 2"]
        J1(("h1"))
        J2(("h2"))
        J3(("h3"))
    end
    subgraph Output["Output Layer"]
        O1(("y1"))
        O2(("y2"))
    end
    I1 --> H1 & H2 & H3 & H4
    I2 --> H1 & H2 & H3 & H4
    I3 --> H1 & H2 & H3 & H4
    H1 --> J1 & J2 & J3
    H2 --> J1 & J2 & J3
    H3 --> J1 & J2 & J3
    H4 --> J1 & J2 & J3
    J1 --> O1 & O2
    J2 --> O1 & O2
    J3 --> O1 & O2
```

### 4. Convolutional Neural Network (Courses 03 and 05)

```mermaid
flowchart LR
    A["Input Image<br/>28x28x1"] --> B["Conv2D<br/>filters, kernel"]
    B --> C["ReLU"]
    C --> D["MaxPooling"]
    D --> E["Conv2D"]
    E --> F["ReLU"]
    F --> G["MaxPooling"]
    G --> H["Flatten"]
    H --> I["Dense<br/>ReLU"]
    I --> J["Dropout"]
    J --> K["Dense<br/>Softmax"]
    K --> L["Class Probabilities"]
```

### 5. Transfer Learning (Courses 03 and 05)

```mermaid
flowchart LR
    subgraph Pretrained["Pretrained Model, frozen"]
        P1["Conv Blocks<br/>feature extractor"]
    end
    subgraph New["New Head, trainable"]
        N1["Global Pooling"] --> N2["Dense"] --> N3["Output Layer"]
    end
    A["Your Dataset"] --> P1
    P1 --> N1
    N3 --> R["Predictions"]
```

### 6. Transformer Architecture (Course 09)

```mermaid
flowchart TD
    A["Input Tokens"] --> B["Token Embedding"]
    B --> C["+ Positional Encoding"]
    C --> D

    subgraph Block["Transformer Block, repeated N times"]
        D["Multi-Head Self-Attention"] --> E["Add and LayerNorm"]
        E --> F["Feed-Forward Network"]
        F --> G["Add and LayerNorm"]
    end

    G --> H["Linear Layer"]
    H --> I["Softmax"]
    I --> J["Next-Token Probabilities"]
```

### 7. Self-Attention Mechanism (Course 09)

```mermaid
flowchart LR
    X["Input Embeddings X"] --> Q["Q = X · Wq"]
    X --> K["K = X · Wk"]
    X --> V["V = X · Wv"]
    Q --> S["Scores = Q · Kᵀ / √d"]
    K --> S
    S --> SM["Softmax"]
    SM --> O["Output = Weights · V"]
    V --> O
```

### 8. LLM Data Preparation Pipeline (Course 07)

```mermaid
flowchart LR
    A["Raw Text Corpus"] --> B["Cleaning<br/>dedupe, normalize"]
    B --> C["Tokenizer<br/>BPE, WordPiece"]
    C --> D["Token IDs"]
    D --> E["Padding and Truncation"]
    E --> F["Dataset and DataLoader"]
    F --> G["Batches to Model"]
```

### 9. Fine-Tuning with LoRA (Courses 10 and 11)

```mermaid
flowchart TD
    A["Pretrained LLM<br/>weights frozen"] --> C["Combine"]
    B["LoRA Adapters<br/>small trainable matrices A and B"] --> C
    D["Task Dataset<br/>instructions and responses"] --> E["Training Loop<br/>SFTTrainer"]
    C --> E
    E --> F["Trained Adapters"]
    F --> G["Merge or Load Adapters"]
    G --> H["Fine-Tuned Model"]
    H --> I["Evaluation<br/>perplexity, benchmarks"]
```

### 10. RLHF and DPO Alignment (Course 11)

```mermaid
flowchart LR
    subgraph RLHF
        A["SFT Model"] --> B["Generate Responses"]
        B --> C["Human Preference Ranking"]
        C --> D["Reward Model"]
        D --> E["PPO Optimization"]
        E --> F["Aligned Model"]
    end
    subgraph DPO
        G["SFT Model"] --> H["Preference Pairs<br/>chosen vs rejected"]
        H --> I["Direct Preference<br/>Optimization"]
        I --> J["Aligned Model"]
    end
```

### 11. RAG Pipeline (Courses 12 and 13)

```mermaid
flowchart TD
    subgraph Ingestion["Ingestion, offline"]
        A["Documents<br/>PDF, web, text"] --> B["Loader"]
        B --> C["Text Splitter<br/>chunks"]
        C --> D["Embedding Model"]
        D --> E[("Vector Store<br/>Chroma, FAISS")]
    end

    subgraph Query["Query, online"]
        Q["User Question"] --> QE["Embed Question"]
        QE --> R["Retriever<br/>top-k similarity search"]
        E --> R
        R --> P["Prompt<br/>question + retrieved context"]
        P --> L["LLM"]
        L --> ANS["Answer with Sources"]
    end
```

### 12. RAG Request Sequence

```mermaid
sequenceDiagram
    participant U as User
    participant App as App / LangChain
    participant Emb as Embedding Model
    participant VS as Vector Store
    participant LLM as LLM

    U->>App: Ask a question
    App->>Emb: Embed the question
    Emb-->>App: Query vector
    App->>VS: Similarity search, top k
    VS-->>App: Relevant chunks
    App->>LLM: Prompt with question and chunks
    LLM-->>App: Generated answer
    App-->>U: Answer with sources
```

### 13. AI Agent Loop (Course 12)

```mermaid
flowchart TD
    A["User Goal"] --> B["LLM Reasons<br/>what to do next"]
    B --> C{"Need a tool?"}
    C -->|"yes"| D["Select Tool<br/>search, calculator, retriever, API"]
    D --> E["Execute Tool"]
    E --> F["Observation"]
    F --> B
    C -->|"no"| G["Final Answer"]
```

### 14. Capstone Project System (Course 13)

```mermaid
flowchart LR
    subgraph Frontend
        UI["Web UI<br/>Streamlit, Gradio"]
    end
    subgraph Backend
        CH["LangChain<br/>Retrieval Chain"]
        MEM["Conversation Memory"]
    end
    subgraph Data
        DL["Document Loader"]
        VS[("Vector DB")]
    end
    subgraph Models
        EM["Embedding Model"]
        LM["LLM"]
    end

    UI <--> CH
    CH <--> MEM
    CH --> VS
    CH --> LM
    DL --> EM --> VS
```

---

## 📓 Notebook Format

Every notebook follows one consistent structure:

```mermaid
flowchart TD
    A["1. Title and Learning Objectives"] --> B["2. Concept<br/>theory in plain English"]
    B --> C["3. Imports<br/>each one explained"]
    C --> D["4. Code Cell"]
    D --> E["5. Line-by-Line Explanation<br/>table under every code cell"]
    E --> F{"More code<br/>for this topic?"}
    F -->|"yes"| D
    F -->|"no"| G["6. Output Interpretation"]
    G --> H["7. Common Mistakes"]
    H --> I["8. Key Takeaways"]
    I --> J["9. Practice Exercise"]
```

### Line-by-line example

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

| Part | What it does | Why |
|---|---|---|
| `train_test_split(X, y, ...)` | Randomly splits features and labels into two sets | Test on data the model has never seen |
| `test_size=0.2` | 20% goes to the test set, 80% to training | Standard split ratio |
| `random_state=42` | Fixes the shuffle seed | Same split every run |
| `X_train, X_test, y_train, y_test` | Four outputs unpacked in order | Training and test features and labels |

---

## 🛠 Tech Stack

| Area | Tools |
|---|---|
| Language | Python 3.10+ |
| Data | NumPy, Pandas, SciPy |
| Visualization | Matplotlib, Seaborn |
| Classical ML | scikit-learn |
| Deep learning | TensorFlow, Keras, PyTorch, torchvision |
| NLP and LLMs | Hugging Face Transformers, Datasets, Tokenizers |
| Fine-tuning | PEFT, TRL, Accelerate |
| RAG and agents | LangChain, ChromaDB, FAISS |
| Apps | Streamlit |
| Environment | JupyterLab, venv, Git, GitHub |

```mermaid
flowchart TB
    subgraph Apps["Application Layer"]
        ST["Streamlit"]
    end
    subgraph Orchestration["Orchestration Layer"]
        LC["LangChain"]
    end
    subgraph Models["Model Layer"]
        TF["TensorFlow / Keras"]
        PT["PyTorch"]
        HF["Hugging Face<br/>Transformers, PEFT, TRL"]
        SK["scikit-learn"]
    end
    subgraph Data["Data Layer"]
        NP["NumPy / Pandas / SciPy"]
        VDB["ChromaDB / FAISS"]
    end
    subgraph Env["Environment"]
        PY["Python 3.10+, JupyterLab, Git"]
    end

    ST --> LC
    LC --> HF
    LC --> VDB
    HF --> PT
    TF --> NP
    PT --> NP
    SK --> NP
    NP --> PY
    VDB --> PY
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or newer
- Git
- About 10 GB of free disk space (more if you train large models)
- Optional: NVIDIA GPU with CUDA for the PyTorch, TensorFlow and fine-tuning courses

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/abhirajbalyan/ai-engineer-specialization.git
cd ai-engineer-specialization

# 2. Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate

# 3. Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

# 4. Register the Jupyter kernel
python -m ipykernel install --user --name ai-eng --display-name "Python (ai-eng)"

# 5. Launch JupyterLab
jupyter lab
```

### Install per course (lighter setup)

| Courses | Install |
|---|---|
| 01 | `pip install numpy pandas scipy scikit-learn matplotlib seaborn jupyterlab` |
| 02, 03 | `pip install tensorflow keras` |
| 04, 05 | `pip install torch torchvision torchaudio` |
| 07 to 11 | `pip install transformers datasets tokenizers peft trl accelerate` |
| 12, 13 | `pip install langchain langchain-community chromadb faiss-cpu python-dotenv streamlit` |

### Environment variables

Courses that call hosted model APIs need keys. Create a `.env` file in the repo root (it is git-ignored):

```
OPENAI_API_KEY=your_key_here
HUGGINGFACEHUB_API_TOKEN=your_token_here
```

Load them in a notebook:

```python
from dotenv import load_dotenv
load_dotenv()
```

### How to navigate

1. Open a course folder, for example `01-machine-learning-with-python/`.
2. Read its `README.md` for the module list.
3. Open `notebooks/` and go in numeric order.
4. Read `notes/` for the theory behind each notebook.
5. Check the graded work in `project/`.

---

## 🔄 Workflow

### Building the repo, per course

```mermaid
flowchart LR
    A["Watch lesson"] --> B["Create notebook"]
    B --> C["Write concept<br/>in own words"]
    C --> D["Code in small cells"]
    D --> E["Add line-by-line<br/>explanations"]
    E --> F["Restart and Run All"]
    F -->|"errors"| D
    F -->|"clean"| G["Save theory notes<br/>and project work"]
    G --> H["git add, commit, push"]
    H --> I["Update course README<br/>and progress tracker"]
```

### Git workflow

```mermaid
gitGraph
    commit id: "Initial structure"
    branch course-01
    checkout course-01
    commit id: "Add regression notebook"
    commit id: "Add classification notebook"
    commit id: "Add course 01 notes"
    checkout main
    merge course-01 id: "Complete course 01"
    branch course-02
    checkout course-02
    commit id: "Add perceptron notebook"
    commit id: "Add Keras models"
    checkout main
    merge course-02 id: "Complete course 02"
```

### Commit message convention

```
Add <what> (course NN)
Update <what> (course NN)
Fix <what> in <file>
Docs: update README progress
```

---

## ✅ Progress Tracker

Status key: ⬜ not started · 🟨 in progress · ✅ complete

| # | Course | Notebooks | Notes | Labs | Project | Status |
|---|---|---|---|---|---|---|
| 01 | Machine Learning with Python | 0 | 0 | 0 | 0 | ⬜ |
| 02 | Intro to Deep Learning with Keras | 0 | 0 | 0 | 0 | ⬜ |
| 03 | Deep Learning with Keras and TensorFlow | 0 | 0 | 0 | 0 | ⬜ |
| 04 | Intro to Neural Networks and PyTorch | 0 | 0 | 0 | 0 | ⬜ |
| 05 | Deep Learning with PyTorch | 0 | 0 | 0 | 0 | ⬜ |
| 06 | AI Capstone Project | 0 | 0 | 0 | 0 | ⬜ |
| 07 | GenAI and LLMs: Architecture and Data Prep | 0 | 0 | 0 | 0 | ⬜ |
| 08 | Gen AI Foundational Models for NLP | 0 | 0 | 0 | 0 | ⬜ |
| 09 | GenAI Language Modeling with Transformers | 0 | 0 | 0 | 0 | ⬜ |
| 10 | GenAI Engineering and Fine-Tuning | 0 | 0 | 0 | 0 | ⬜ |
| 11 | GenAI Advanced Fine-Tuning for LLMs | 0 | 0 | 0 | 0 | ⬜ |
| 12 | AI Agents Using RAG and LangChain | 0 | 0 | 0 | 0 | ⬜ |
| 13 | Project: GenAI Apps with RAG and LangChain | 0 | 0 | 0 | 0 | ⬜ |

```mermaid
gantt
    title Completion Plan
    dateFormat  YYYY-MM-DD
    axisFormat  %b %d
    section Classical ML
    Course 01           :c1, 2026-11-15, 10d
    section Deep Learning
    Course 02           :c2, after c1, 5d
    Course 03           :c3, after c2, 11d
    Course 04           :c4, after c3, 10d
    Course 05           :c5, after c4, 10d
    Course 06           :c6, after c5, 8d
    section Generative AI
    Course 07           :c7, after c6, 3d
    Course 08           :c8, after c7, 5d
    Course 09           :c9, after c8, 5d
    Course 10           :c10, after c9, 4d
    Course 11           :c11, after c10, 5d
    section RAG and Agents
    Course 12           :c12, after c11, 5d
    Course 13           :c13, after c12, 5d
```

> Adjust the start dates in the Gantt block to match your actual schedule.

---

## 🎓 Skills Matrix

| Skill | Courses | Level |
|---|---|---|
| Data wrangling (Pandas, NumPy) | 01 | ⭐⭐⭐⭐ |
| Supervised and unsupervised ML | 01 | ⭐⭐⭐⭐ |
| Model evaluation and tuning | 01 | ⭐⭐⭐⭐ |
| Neural networks from scratch | 02, 04 | ⭐⭐⭐⭐ |
| Keras and TensorFlow | 02, 03 | ⭐⭐⭐⭐ |
| PyTorch | 04, 05 | ⭐⭐⭐⭐ |
| CNNs and computer vision | 03, 05, 06 | ⭐⭐⭐⭐ |
| Sequence models | 03, 08 | ⭐⭐⭐ |
| Tokenization and embeddings | 07 | ⭐⭐⭐⭐ |
| Transformers and attention | 09 | ⭐⭐⭐⭐ |
| Hugging Face ecosystem | 10, 11 | ⭐⭐⭐⭐ |
| PEFT, LoRA, fine-tuning | 10, 11 | ⭐⭐⭐⭐ |
| RLHF and DPO | 11 | ⭐⭐⭐ |
| RAG systems | 12, 13 | ⭐⭐⭐⭐ |
| AI agents and tool use | 12 | ⭐⭐⭐ |
| LangChain apps | 12, 13 | ⭐⭐⭐⭐ |

> Update the star levels as you complete each course.

---

## 🧭 Roadmap

- [ ] Set up repo structure and templates
- [ ] Complete courses 01 to 03 (ML and Keras)
- [ ] Complete courses 04 to 06 (PyTorch and capstone)
- [ ] Complete courses 07 to 09 (LLM foundations and transformers)
- [ ] Complete courses 10 and 11 (fine-tuning)
- [ ] Complete courses 12 and 13 (RAG and agents)
- [ ] Add a unified glossary in `docs/GLOSSARY.md`
- [ ] Add CI to check that every notebook runs
- [ ] Publish a rendered documentation site with GitHub Pages
- [ ] Tag release `v1.0`

---

## 🤝 Contributing

Suggestions and corrections are welcome.

1. Fork the repository
2. Create a branch: `git checkout -b fix/typo-in-course-03`
3. Commit your changes: `git commit -m "Fix typo in course 03 notes"`
4. Push: `git push origin fix/typo-in-course-03`
5. Open a Pull Request

Please keep notebooks in the standard format described in `docs/NOTEBOOK_TEMPLATE.md`.

---

## 📄 License

Released under the [MIT License](LICENSE).

Course content and materials belong to their respective creators and instructors. This repository contains only original notes, explanations and personal solutions, for educational purposes.

---

## 👤 Author

**Abhiraj**

- GitHub: [@abhirajbalyan](https://github.com/abhirajbalyan)

---

<div align="center">

⭐ If this repo helps you, consider giving it a star.

</div>
