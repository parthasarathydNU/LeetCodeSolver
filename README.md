# DSA Problem Solver - a system that outperforms ChatGPT in solving unseen leetcode medium and hard problems

## Overview

The **DSA Problem Solver** project aims to simplify the process of solving Data Structures and Algorithms (DSA) problems by leveraging advanced language models and retrieval-augmented generation (RAG) techniques. This tool is designed to assist users in tackling challenging DSA problems, making the process more intuitive and less daunting.


### Current Approach:

Open to suggestions:


```mermaid
flowchart TD
    A[Start] --> B[Generate problem approach]
    B --> C[Generate pseudo code]
    C --> D[Generate Python code with test cases]
    D --> E[Initialize variables]
    E --> F{Tries <= 5 and\nnot solved?}
    F -->|Yes| G[Attempt to execute code]
    G --> H{Execution successful\nand all tests passed?}
    H -->|No| I[Handle Failure]
    I --> J[Update Python code]
    J --> F
    H -->|Yes| K[Mark as solved]
    K --> F
    F -->|No| L[Return results]
    L --> M[End]

    style F decision
    style H decision
```

```mermaid
flowchart TD
    A[Start handleFailure] --> C[Trying to correct the code]
    C --> D[Get code corrector prompts with test case failure and error messages]
    D --> E[Initialize LLM with OpenAI GPT-4]
    E --> F[Generate corrected code with test cases using LLM]
    F --> G[Extract and process corrected code with tests]
    G --> I[Return corrected code]
    I --> J[Return corrected code]
    J --> K[End handleFailure]
```

## Features

- **Agentic LLM Integration**: Utilizes language models to understand and generate solutions for various DSA problems by breaking it down into simpler steps
- **Retrieval-Augmented Generation (RAG)**: Enhances problem-solving capabilities by combining retrieval of latest information on the internet to support generation of tailored solutions.
- **Code Execution**: Uses native python engine to eecute code and test cases to enable iterative improvements based on error messages / test case failure

## Challenges

- **Getting an LLM to understand logic**
- **To break the barrier - the system is as good as the LLM used**

## Usage

1. **Input Problem Statement**:
   Provide the DSA problem statement either via the command line interface or through the web interface.

2. **Receive Solution**:
   The tool will analyze the problem using the Agentic LLM and RAG techniques, then provide a detailed solution with explanations.

3. **Explore Solutions**:
   Users can review the solutions and explanations, use the playground to test the solution and interact with the tool for further clarification or alternative approaches.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or support, feel free to reach out.
