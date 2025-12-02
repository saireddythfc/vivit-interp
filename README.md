# vivit-interp
Causal Analysis of Video Vision Transformer:

***Accepted at AAAI 2026 Deployable AI Workshop***

The paper explores how video models trained for classification tasks represent nuanced, hidden semantic information that may not affect the final outcome, a key challenge for Trustworthy AI models. Through Explainable and Interpretable AI methods, specifically mechanistic interpretability techniques, the internal circuit responsible for representing the action’s outcome is reverse-engineered in a pre-trained video vision transformer, revealing that the ”Success vs Failure” signal is computed through a distinct amplification cascade. While there are low-level differences observed from layer 0, the abstract and semantic representation of the outcome is progressively amplified from layers 5 through 11.

Causal analysis, primarily using activation patching supported by ablation results, reveals a clear division of labor:
Attention Heads act as ”evidence gatherers”, providing necessary low-level information for partial signal recovery, while MLP Blocks function as robust ”concept composers”, each of
which is the primary driver to generate the ”success” signal.

This distributed and redundant circuit in the model’s internals explains its resilience to simple ablations, demonstrating a core computational pattern for processing human-action
outcomes. Crucially, the existence of this sophisticated circuit for representing complex outcomes, even within a model trained only for simple classification, highlights the potential for models to develop forms of ’hidden knowledge’ beyond their explicit task, underscoring the need for mechanistic oversight for building genuinely Explainable and Trustworthy AI systems intended for deployment.

