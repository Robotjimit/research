---

## 🔑 使用指南

1.  **选择提示词**: 根据需要写作的章节或任务，找到相应的提示词。
2.  **准备输入**: 收集必要的信息，如研究主题、背景、方法、数据、结果等。
3.  **填充提示词**: 将提示词复制到对话框，并替换 `{}` 中的内容。
4.  **迭代优化**: 对生成的 LaTeX 代码进行微调，以达到最佳效果。

---

## 📖 核心提示词列表

### 1. Abstract （摘要）

**提示词:**
你是一名学术论文写作专家，请以 CNS 期刊的风格撰写学术摘要。请严格以 LaTeX 代码格式生成内容，所有数学公式和图表代码必须符合 LaTeX 语法。

**输入:**
-   **研究主题:** {topic}
-   **研究背景:** {background}
-   **提出的方法:** {method}
-   **使用的数据集/实验环境:** {dataset}
-   **主要结果:** {results}
-   **贡献总结:** {contributions}

**输出要求:**
-   生成一段 200–300 字的摘要。
-   使用 `\begin{abstract} ... \end{abstract}` 环境。
-   内容简洁、逻辑清晰，避免无意义的修饰。

---

### 2. Introduction （引言）

**提示词:**
你是一名学术论文写作专家，请以 CNS 期刊的风格撰写 Introduction。请严格以 LaTeX 代码格式生成内容。

**输入:**
-   **研究主题:** {topic}
-   **背景信息:** {background}
-   **已有研究文献列表:** {bib_file_or_list}
-   **本文方法:** {method}
-   **核心贡献:** {contributions}

**输出要求:**
-   章节标题使用 `\section{Introduction}`。
-   **第一段**: 阐述 `{topic}` 的重要性和背景。
-   **第二至三段**: 总结现有方法，并使用 `\cite{...}` 命令引用我提供的文献。
-   **第四段**: 明确指出现有方法的不足和挑战。
-   **第五段**: 提出本文的解决方案 `{method}` 和主要贡献。
-   **贡献总结**: 使用 `\begin{itemize} ... \end{itemize}` 环境，将贡献点作为列表呈现。

---

### 3. Related Work （相关工作）

**提示词:**
你是一名学术论文写作专家，请撰写 Related Work 部分，风格为 CNS 期刊。请严格以 LaTeX 代码格式生成内容。

**输入:**
-   **研究领域:** {field}
-   **参考文献列表:** {bib_file_or_list}
-   **本文方法:** {method}

**输出要求:**
-   章节标题使用 `\section{Related Work}`。
-   概述相关领域与任务背景。
-   按研究方向或方法分类总结，使用 `\subsection{...}`。
-   强调已有方法的不足与挑战。
-   清晰说明本文与现有工作的差异与优势。

---

### 4. Methods （方法）

**提示词:**
你是一名学术论文写作专家，请以严谨的学术风格撰写 Methods 部分，并严格以 LaTeX 代码格式输出。

**输入:**
-   **问题定义:** {problem_definition}
-   **模型概述:** {model_description}
-   **算法伪代码:** {pseudocode_text}
-   **关键公式描述:** {formula_description}

**输出要求:**
-   章节标题使用 `\section{Methods}`。
-   **子章节**：
    -   `\subsection{Problem Definition}`: 定义研究问题和符号。
    -   `\subsection{Model Architecture}`: 描述总体框架和各模块。
    -   `\subsection{Loss Function and Training}`: 给出损失函数公式。
    -   `\subsection{Algorithm}`: 给出伪代码。
-   **公式**: 使用 `\begin{equation} ... \end{equation}` 环境。
-   **伪代码**: 使用 `\begin{algorithm} ... \end{algorithm}` 环境。

---

### 5. Experiments （实验）

**提示词:**
你是一名学术论文写作专家，请生成 Experiments 部分，风格为 CNS。请严格以 LaTeX 代码格式生成内容。

**输入:**
-   **数据集信息:** {dataset_info}
-   **实验设置:** {settings}
-   **评价指标:** {metrics_with_formulas}
-   **实验结果数据:** {result_table_in_text}
-   **消融实验数据:** {ablation_study_data}

**输出要求:**
-   章节标题使用 `\section{Experiments}`。
-   **子章节**：
    -   `\subsection{Datasets and Experimental Setup}`: 数据集来源、划分和参数设置。
    -   `\subsection{Evaluation Metrics}`: 列出评价指标及其 LaTeX 公式。
    -   `\subsection{Main Results}`: 描述实验结果，并生成对应的 `\begin{table}` 表格。
    -   `\subsection{Ablation Study}`: 解释关键模块的贡献。
-   **表格**: 使用 `\begin{table} ... \end{table}` 环境。

---

### 6. Results & Discussion （结果与讨论）

**提示词:**
你是一名学术论文写作专家，请撰写 Results & Discussion 部分，并严格以 LaTeX 代码格式输出。

**输入:**
-   **对比实验结果:** {comparison_results}
-   **可视化图表描述:** {figure_descriptions}
-   **案例分析:** {case_study_details}
-   **方法局限性:** {limitations_and_future_work}

**输出要求:**
-   章节标题使用 `\section{Results and Discussion}`。
-   **结构**：
    -   总结对比实验优势，突出关键指标提升。
    -   根据提供的描述，撰写图例（`\caption`）并解释图表。
    -   通过具体案例展示方法有效性。
    -   讨论方法的局限性与未来方向。
-   **引用图表**: 使用 `\ref{fig:...}` 和 `\ref{tab:...}` 命令。

---

### 7. Conclusion （结论）

**提示词:**
你是一名学术论文写作专家，请以 CNS 期刊的风格撰写结论部分，并严格以 LaTeX 代码格式输出。

**输入:**
-   **研究问题:** {research_question}
-   **提出的方法:** {method}
-   **核心贡献:** {key_contributions}
-   **未来展望:** {future_work_directions}

**输出要求:**
-   章节标题使用 `\section{Conclusion}`。
-   回顾研究问题、提出的方法和主要贡献。
-   展望未来的研究方向（如扩展、跨模态、实际应用等）。

---

## 🛠 通用工具类提示词

### 语言润色

**提示词:**
你是一名英语母语的学术论文写作专家，请帮我润色以下段落，使其符合 CNS 期刊的风格。请严格以 LaTeX 代码格式输出。

**输入:** {paragraph_to_polish}

### 翻译

**提示词:**
你是一名学术论文写作专家，请将以下中文段落翻译为英文，要求符合 CNS 期刊的学术论文表达规范。请严格以 LaTeX 代码格式输出。

**输入:** {chinese_paragraph}

### 表格生成

**提示词:**
你是一名学术论文写作专家，请将以下实验数据转换为美观且标准的 LaTeX 表格代码。

**输入:**
-   **数据:** {data_in_text_or_csv}
-   **表格标题:** {table_caption}
-   **表格标签:** {table_label}

**输出要求:**
-   使用 `\begin{table}[h!] ... \end{table}` 环境。
-   包含 `\caption{...}` 和 `\label{...}`。
-   根据数据类型选择合适的 `tabular` 列格式。

### 数学公式生成

**提示词:**
你是一名学术论文写作专家，请根据以下描述生成完整的 LaTeX 数学公式代码。

**输入:**
-   **公式描述:** {formula_description}
-   **公式标签:** {formula_label}

**输出要求:**
-   使用 `\begin{equation} ... \end{equation}` 环境。
-   包含 `\label{...}` 以便引用。

### 审稿应答

**提示词:**
你是一名学术论文写作专家，请帮我生成对审稿人评论的回复。请严格以 LaTeX 代码格式输出，并使用 `\begin{itemize}` 或 `\enumerate` 环境组织回复。

**输入:**
-   **审稿人意见:** {reviewer_comments_text}
-   **你的回复与修改说明:** {your_responses_and_revisions}

**输出要求:**
-   语气礼貌、尊重。
-   逐条回应审稿人提出的问题。
-   清晰说明已做的修改与补充实验。
-   在回复中引用审稿人意见，例如使用 `\textit{Reviewer: ...}`。

### code
作为一名专业的软件工程师和代码分析师，你的任务是分析一个给定代码库的代码结构，并生成一份详细的摘要。

请根据以下步骤完成你的分析和报告：

第一步：代码库概览
首先，请提供一个简短的概览，描述这个代码库的主要目的、技术栈以及整体架构。

第二步：文件级别分析
对于代码库中的每个文件，请进行以下分析：

文件路径：提供完整的文件路径。

功能摘要：用一到两句话简要概括该文件的核心功能。

主要函数/类：列出文件中最重要的函数、方法或类，并用简短的注释说明其作用。

文件间的依赖关系：说明该文件导入了哪些其他文件或库，以及它被哪些文件所依赖（如果信息可用）。

第三步：模块/目录级别总结
将相关的文件组织成逻辑模块或目录，并为每个模块提供一个简短的总结。

模块名称：例如，“用户认证模块”、“数据处理模块”等。

核心功能：描述该模块负责的主要任务。

关键文件：列出该模块中最关键的几个文件。

第四步：整体代码结构总结
综合以上分析，生成一个关于代码库整体结构的总结。

设计模式：识别并描述代码库中使用的任何常见设计模式（如MVC、单例、工厂模式等）。

优点与不足：分析当前代码结构的好处（如可维护性、可扩展性）和潜在的不足之处（如冗余、复杂性）。

改进建议：基于你的分析，提供一些关于如何优化代码结构的具体建议。

报告格式要求
请将以上内容以清晰的Markdown格式呈现，使用标题、列表和粗体字来提高可读性。
