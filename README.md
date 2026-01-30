# Bachelor Thesis: Platform Engineering and KubePattern
### Engineering the Golden Path for Cloud Native Development

This repository contains the source code, pattern definitions, and final report for my Bachelor's Thesis in Computer Science at the **University of Milano-Bicocca**.

The project was conducted during my internship at **Sigemi** (Kubecloud Division) and focuses on two core engineering achievements:
1.  **KubePattern:** A novel, graph-based automated analysis tool for Kubernetes.
2.  **Platform Engineering:** The evolution of Sigemi's Internal Developer Platform (IDP).

## 📂 Repository Structure

* **[`/pattern-registry`](./pattern-registry)**
    A standalone, persistent snapshot of the **"Pattern as Code"** definitions designed for this thesis. It contains the JSON schemas and logic used to detect architectural smells (e.g., *Predictable Demands*, *Health Probe*, *Sidecar*).
    > *Note: KubePattern has been released as open-source. For the latest live registry, visit the [Official KubePattern Repository](https://github.com/kubepattern/registry).*

* **[`/thesis-latex`](./thesis-latex)**
    The complete LaTeX source code used to generate the academic report.

* **[`thesis-final.pdf`](./thesis-final.pdf)**
    The final compiled version of the thesis document.

## 🚀 Abstract
The rapid evolution of Cloud Native architectures has established Kubernetes as the de-facto standard for container orchestration. However, its inherent complexity and steep learning curve present significant operational challenges, often hindering development velocity and introducing technical debt. In this context, Platform Engineering emerges as a critical discipline to mitigate these issues by building Internal Developer Platforms (IDPs) that reduce cognitive load and enforce compliance through automated "Golden Paths".

This thesis details the engineering of **KubePattern**, an automated analysis tool designed to identify architectural "smells" and enforce best practices within Kubernetes clusters. KubePattern employs a **graph-based approach**, modeling cluster resources and their relationships to detect misconfigurations that isolated manifest analysis cannot perceive. The tool leverages a "Pattern as Code" methodology, retrieving declarative smell definitions from a central registry.

Additionally, the work documents the integration of KubePattern into Sigemi's CI/CD pipeline, adopting a "Platform for Platform" approach. The result is a system that ensures compliance, reliability, and serves as an educational tool for Cloud Native adoption.

## 🛠️ Engineering Contribution
My work focused on the **design and implementation** of the following systems:

# KubePattern
* **Graph-Based Engine:** Implemented using **JGraphT** to model Kubernetes resources (Vertices) and relationships (Edges) like `OWNS`, `MOUNTS`.
* **Pattern as Code:** Designed a JSON-based schema to decouple detection logic from the core engine, allowing dynamic updates from a remote registry.
* **Tech Stack:** Built with **Java** and **Spring Boot**, utilizing the **Official Kubernetes Java Client** for performance-oriented cluster interactions.

## 💻 Technology Stack

| Category | Technologies Used |
| :--- | :--- |
| **Core Languages** | **Java** (Spring Boot) |
| **Platform** | **Kubernetes** |
| **Libraries** | JGraphT, Official K8s Java Client, JSONPath |

## 📄 License
This thesis is open-source. The patterns contained herein are derived from the [KubePattern Project](https://github.com/kubepattern).
The KubePattern source code is licensed under **Apache V2.0**.
