# Literature Overview
_Last updated: 19/09/2025_

This document summarizes the key sources collected for the dissertation.  
They are grouped into categories for easier navigation. To be updated.

---
## 📚 Surveys — GNNs & Bioinformatics

1. **Xiao-Meng Zhang; Li Liang; Lin Liu; Ming-Jing Tang**  
   *Graph Neural Networks and Their Current Applications in Bioinformatics* (2021).  
   Systematic survey of GNN models and principles; maps tasks (node classification, link prediction, graph generation) to bio apps across disease prediction, drug discovery, and biomedical imaging; flags data quality, methodology, and interpretability as key challenges.

2. **Michail Chatzianastasis; Michalis Vazirgiannis; Zijun Zhang**  
   *Explainable Multilayer Graph Neural Network for cancer gene prediction* (2023).  
   Though an application paper, it doubles as an explainable GNN case study for genomics: multilayer graph learning over multiple gene–gene networks with pan-cancer omics; demonstrates improved accuracy and interpretability.

3. **Sezin Kircali Ata; Min Wu; Yuan Fang; Le Ou-Yang; Chee Keong Kwoh; Xiao-Li Li**  
   *Recent Advances in Network-based Methods for Disease Gene Prediction* (2020/2021).  
   Comprehensive review of network diffusion, classic ML with graph features, and graph representation learning for disease-gene prediction; includes empirical comparison of 14 methods across seven diseases and outlines future directions.

4. **Julia Åkesson; Zelmina Lubovac-Pilav; Rasmus Magnusson; Mika Gustafsson**  
   *ComHub: Community predictions of hubs in gene regulatory networks* (2021).  
   Application/benchmark-focused work that reads like a mini-survey on hub inference: ensembles multiple GRN methods to robustly identify TF hubs; strong performance on DREAM5 + independent datasets.

5. **Hung Nguyen; Duc Tran; Bang Tran; Bahadir Pehlivan; Tin Nguyen**  
   *A comprehensive survey of regulatory network inference methods using single cell RNA sequencing data* (2020).  
   Reviews 15 scRNA-seq GRN tools, detailing assumptions, algorithms, usability, and robustness to dropout; extensive simulations + practical guidance on method selection and complexity.

6. **Mengyuan Zhao; Wenying He; Jijun Tang; Quan Zou; Fei Guo**  
   *A comprehensive overview and critical evaluation of gene regulatory network inference technologies* (2021).  
   Broad survey of GRN reconstruction across model-, information-, and ML-based families; standardized benchmarks highlight stability and scaling sensitivities; practical notes for choosing methods for specific GRNs.

7. **Sergi Abadal; Akshay Jain; Robert Guirado; Jorge López-Alonso; Eduard Alarcón**  
   *Computing Graph Neural Networks: A Survey from Algorithms to Accelerators* (2022).  
   Computing-centric survey of GNN fundamentals and end-to-end stacks; analyzes software/hardware acceleration and argues for graph-aware, communication-centric co-design—useful context for scaling bio GNN workloads.

8. **Zonghan Wu; Shirui Pan; Fengwen Chen; Guodong Long; Chengqi Zhang; Philip S. Yu**  
   *A Comprehensive Survey on Graph Neural Networks* (2021).  
   Landmark GNN overview introducing a taxonomy (recurrent, convolutional, autoencoder, spatio-temporal); catalogs benchmarks, datasets, and open problems—handy general reference for architecture choices.

9. **Zhenyi Zhu**  
   *A Survey of GNN in Bioinformation Data* (2022, preprint).  
   Introductory review connecting SOTA GNN models to bioinformatics use cases; emphasizes opportunities and outlines future directions tailored to biological data idiosyncrasies.

10. **Zichen Wang; Vassilis N. Ioannidis; Huzefa Rangwala; Tatsuya Arai; Ryan Brand; Mufei Li; Yohei Nakayama**  
    *Graph Neural Networks in Life Sciences: Opportunities and Solutions* (2022, KDD tutorial).  
    Tutorial-style survey of biomedical graph types and problem setups; four hands-on pipelines (small molecules, macromolecules, protein–ligand bi-graphs, KG-driven drug discovery) with DGL tooling for rapid adoption.


---
## 🦠 Disease–Gene Prediction Papers (GNN & Network Approaches)

1. **Feiyue Sun; Jianqiang Sun; Qi Zhao**  
   *A deep learning method for predicting metabolite–disease associations via graph neural network* (2022).  
   Builds a heterogeneous metabolite–disease graph; uses GCN layers with an attention-based aggregator (GCNAT) to fuse multi-layer embeddings. Achieves AUROC ≈0.95 and PR ≈0.405, outperforming 5 baselines. Case studies validate predicted metabolite–disease links.

2. **Haohui Lu; Shahadat Uddin**  
   *A weighted patient network-based framework for predicting chronic diseases using graph neural networks* (2021).  
   Projects patient–disease bipartite graphs to a weighted patient network. GNNs with attention learn patient embeddings for chronic disease prediction. Accuracy: ~93.5% (CVD), ~89.1% (COPD). Visualizations show strong cohort separability.

3. **Zhen Gao; Yansen Su; Junfeng Xia; Rui-Fen Cao; Yun Ding; Chun-Hou Zheng; Pi-Jing Wei**  
   *DeepFGRN: inference of gene regulatory network with regulation type based on directed graph embedding* (2024).  
   Infers directed GRNs with regulation type using bidirectional node representation, adversarial neighbor learning, and correlation modules. Identifies candidate biomarkers/therapeutics in breast, liver, lung cancer, and COVID-19.

4. **Laura Cantini; Enzo Medico; Santo Fortunato; Michele Caselle**  
   *Detection of gene communities in multi-networks reveals cancer drivers* (2015).  
   Integrates TF co-targeting, miRNA co-targeting, PPI, and co-expression into multi-networks. Consensus clustering finds known and novel cancer driver genes, highlighting regulatory patterns across gastric, lung, pancreas, and colorectal cancer.

5. **Zhenchao Sun; Hongzhi Yin; Hongxu Chen; Tong Chen; Lizhen Cui; Fan Yang**  
   *Disease Prediction via Graph Neural Networks* (2021).  
   Constructs medical concept and patient record graphs; GNN encoder aggregates both to handle rare diseases and cold-start patients. Improves prediction by fusing EMRs with external knowledge bases.

6. **Michail Chatzianastasis; Michalis Vazirgiannis; Zijun Zhang**  
   *Explainable Multilayer Graph Neural Network for cancer gene prediction* (2023).  
   Multilayer GNN across multiple gene–gene networks with pan-cancer omics. Improves accuracy and interpretability, addressing instability across network choices.

7. **Yijuan Wang; Zhi-Ping Liu**  
   *Identifying biomarkers for breast cancer by gene regulatory network rewiring* (2021).  
   Builds condition-specific GRNs, extracts differential GRN, applies community detection, and selects biomarkers with LR+RFE. Biomarkers achieve AUC up to 0.989 in external validation.

8. **Pietro Cinaglia; Mario Cannataro**  
   *Identifying Candidate Gene–Disease Associations via Graph Neural Networks* (2023).  
   GNN trained on curated gene–disease graphs with multi-layer convolutions. Node embeddings rank candidate GDAs; AUC ≈0.95 with ~93% precision among top-15 DisGeNET predictions.

9. **Fei Liu; Shao-Wu Zhang; Wei-Feng Guo; Ze-Gang Wei; Luonan Chen**  
   *Inference of Gene Regulatory Network Based on Local Bayesian Networks* (2016).  
   Classical GRN inference with local Bayesian networks. Reduces false positives using conditional independence. Baseline approach for regulatory discovery.

10. **Akshata Hegde; Tom Nguyen; Jianlin Cheng**  
    *Machine Learning Methods for Gene Regulatory Network Inference* (2025, preprint).  
    Review of ML/AI methods for GRN inference (supervised, unsupervised, semi, contrastive). Surveys datasets, metrics, and emerging deep learning approaches.

11. **Laura Hernández-Lorenzo; Markus Hoffmann; Evelyn Scheibling; Markus List; Jordi A. Matías-Guiu; Jose L. Ayala**  
    *On the limits of graph neural networks for the early diagnosis of Alzheimer’s disease* (2022).  
    Builds patient-specific PPI subnetworks with variant labels. GNNs outperform classical ML but not APOE-only baseline. Highlights value of gene interactions yet limitations of missense-only features.

12. **Cheng Yan; Guihua Duan; Na Li; Lishen Zhang; Fang-Xiang Wu; Jianxin Wang**  
    *PDMDA: predicting deep-level miRNA–disease associations with graph neural networks and sequence features* (2022).  
    Predicts not only presence but types of miRNA–disease associations. Combines GNNs with sequence features for richer disease mechanism inference.

13. **Vikash Singh; Pietro Lio’**  
    *Towards Probabilistic Generative Models Harnessing Graph Neural Networks for Disease-Gene Prediction* (2019, preprint).  
    Introduces VGAE and constrained-VGAE for unsupervised disease–gene link prediction in heterogeneous g
---

## 🏗️ GNN Architectures & Bioinformatics Surveys

1. **Xiao-Meng Zhang; Li Liang; Lin Liu; Ming-Jing Tang**  
   *Graph Neural Networks and Their Current Applications in Bioinformatics* (2021).  
   Systematic survey of GNNs (models, tasks: node/link/graph) and applications across disease prediction, drug discovery, and biomedical imaging; outlines data-quality, methodology, and interpretability challenges.

2. **Michail Chatzianastasis; Michalis Vazirgiannis; Zijun Zhang**  
   *Explainable Multilayer Graph Neural Network for cancer gene prediction* (2013).  
   Multilayer GNN over multiple gene–gene networks with pan-cancer omics; improves accuracy and provides explanations to address black-box concerns and network choice instability.

3. **Cheng Yan; Guihua Duan; Na Li; Lishen Zhang; Fang-Xiang Wu; Jianxin Wang**  
   *PDMDA: predicting deep-level miRNA–disease associations with graph neural networks and sequence features* (2022).  
   Extends beyond binary links to predict association types; integrates sequence features with GNNs for richer miRNA–disease inference.

4. **Hong Shi; Xiaomeng Zhang; Lin Tang; Lin Liu**  
   *Heterogeneous graph neural network for lncRNA-disease association prediction* (2022).  
   Builds a heterogeneous network (similarities + associations) and uses type-aware neighbor aggregation with attention; achieves strong AUC/AUPR under 5-fold CV.

5. **Sergi Abadal; Akshay Jain; Robert Guirado; Jorge López-Alonso; Eduard Alarcón**  
   *Computing Graph Neural Networks: A Survey from Algorithms to Accelerators* (2022).  
   Computing-centric survey covering GNN fundamentals, ops, software stacks, and hardware accelerators; proposes a communication-centric, graph-aware co-design view.

6. **Zonghan Wu; Shirui Pan; Fengwen Chen; Guodong Long; Chengqi Zhang; Philip S. Yu**  
   *A Comprehensive Survey on Graph Neural Networks* (2021).  
   Landmark survey introducing a taxonomy (recurrent, convolutional, autoencoder, spatio-temporal); catalogs applications, benchmarks, and open directions.

7. **Zhenyi Zhu**  
   *A Survey of GNN in Bioinformation Data* (2022, preprint).  
   Introductory review linking SOTA GNN models to bioinformatics problems; sketches opportunities and future directions specific to bio data.

8. **Zichen Wang; Vassilis N. Ioannidis; Huzefa Rangwala; Tatsuya Arai; Ryan Brand; Mufei Li; Yohei Nakayama**  
   *Graph Neural Networks in Life Sciences: Opportunities and Solutions* (2022, KDD Tutorial).  
   Broad life-sciences tutorial: graph types, problem formulations, and four hands-on GNN pipelines (small molecules, macromolecules, protein–ligand bi-graphs, KG-driven drug discovery).
---
## 🧬 GRN Background

1. **Laura Cantini; Enzo Medico; Santo Fortunato; Michele Caselle**  
   *Detection of gene communities in multi-networks reveals cancer drivers* (2015).  
   Integrates TF co-targeting, miRNA co-targeting, PPI, and co-expression into a multi-network; consensus community detection + enrichment highlights known and novel cancer driver genes across multiple tumor types.

2. **Ting Chen; Vladimir Filkov; Steven S. Skiena**  
   *Identifying gene regulatory networks from experimental data* (1999).  
   Early GRN inference work framing reconstruction from expression data; introduces algorithmic strategies and evaluation ideas that influenced later network-inference methods.

3. **Guy Karlebach; Ron Shamir**  
   *Modelling and analysis of gene regulatory networks* (2008).  
   Seminal review of GRN formalisms (Boolean, Bayesian, differential equation, stochastic) and analysis tasks; sets the conceptual toolkit for GRN modeling.

4. **Fei Liu; Shao-Wu Zhang; Wei-Feng Guo; Ze-Gang Wei; Luonan Chen**  
   *Inference of Gene Regulatory Network Based on Local Bayesian Networks* (2016).  
   Local BN strategy for GRN inference from expression data; leverages conditional independence to prune false positives and improve scalable reconstruction.

5. **Julia Åkesson; Zelmina Lubovac-Pilav; Rasmus Magnusson; Mika Gustafsson**  
   *ComHub: Community predictions of hubs in gene regulatory networks* (2021).  
   Ensemble (“community”) approach that aggregates multiple GRN methods to robustly predict hub TFs; consistently strong on DREAM5 and independent datasets.

6. **Ferdinando Fioretto; Agostino Dovier; Enrico Pontelli**  
   *Constrained Community-Based Gene Regulatory Network Inference* (2015).  
   Meta-predictor that fuses outputs of diverse GRN methods using constraint programming to enforce biological/topological properties, improving accuracy.

7. **Hung Nguyen; Duc Tran; Bang Tran; Bahadir Pehlivan; Tin Nguyen**  
   *A comprehensive survey of regulatory network inference methods using single-cell RNA sequencing data* (2020).  
   Reviews 15 scRNA-seq GRN tools; compares assumptions, robustness to dropout, runtime, and performance on simulations/experiments to guide method choice.

8. **Mengyuan Zhao; Wenying He; Jijun Tang; Quan Zou; Fei Guo**  
   *A comprehensive overview and critical evaluation of gene regulatory network inference technologies* (2021).  
   Broad survey across model-, information-, and ML-based GRN methods; standardized benchmarks reveal stability/sensitivity patterns across network scales.

9. **Thalia E. Chan; Michael P. H. Stumpf; Ann C. Babtie**  
   *Gene Regulatory Network Inference from Single-Cell Data Using Multivariate Information Measures* (2017).  
   Introduces PIDC, using partial information decomposition to capture higher-order dependencies; outperforms pairwise MI on simulations and infers plausible GRNs from single-cell data.

10. **Zhen Gao; Yansen Su; Junfeng Xia; Rui-Fen Cao; Yun Ding; Chun-Hou Zheng; Pi-Jing Wei**  
    *DeepFGRN: inference of gene regulatory network with regulation type based on directed graph embedding* (2024).  
    Deep model for directed, signed GRNs using bidirectional node representations, adversarial neighbor learning, and correlation modules; identifies candidate biomarkers/therapeutics across diseases.

11. **Andrea Mastropietro; Gianluca De Carlo; Aris Anagnostopoulos**  
   *XGDAG: explainable gene–disease associations via graph neural networks* (2023).  
   Proposes an interpretable GNN framework for gene–disease association prediction. Combines deep learning accuracy with mechanisms for transparency, producing ranked gene–disease links while highlighting contributing features. Bridges predictive power and explainability, making outputs more biologically trustworthy.

---
##  🩺 Other Biomedical Applications of GNNs

1. **Haohui Lu; Shahadat Uddin**  
   *A weighted patient network-based framework for predicting chronic diseases using graph neural networks* (2021).  
   Projects patient–disease bipartite graphs into weighted patient networks; GNNs with attention generate patient embeddings. Achieves high accuracy for chronic disease prediction (~93.5% for CVD, ~89.1% for COPD) and reveals separable cohort patterns.

2. **Tianyu Liu; Yuge Wang; Rex Ying; Hongyu Zhao**  
   *MuSe-GNN: Learning Unified Gene Representation From Multimodal Biological Graph Data* (2025).  
   Introduces multimodal similarity learning GNN combining single-cell and spatial transcriptomic data across tissues, species, and sequencing types. Uses contrastive + similarity regularization to unify gene embeddings. Outperforms baselines in functional similarity tasks and aids discovery of pathways, regulatory networks, and disease-related genes.
---


## 📌 Next Steps 
- Mark **most relevant** papers with emphasis (e.g., ★).  
