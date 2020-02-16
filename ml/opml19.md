#  Machine Learning System Notes

## Conference: OpML '19

### Opportunities and Challenges Of Machine Learning Accelerators In Production

[PDF Link](https://www.usenix.org/system/files/opml19papers-ananthanarayanan.pdf)

Comment: nothing important

### TonY: An Orchestrator for Distributed Machine Learning Jobs

[PDF Link](https://www.usenix.org/system/files/opml19papers-hsu.pdf)

1. Initialily, it is a wrapper with YARN, where TonY client submit job and YARN scheduler dispatch job in container to nodes.

### Continuous Training for Production ML in the TensorFlow Extended (TFX) Platform

[PDF Link](https://www.usenix.org/system/files/opml19papers-baylor.pdf)

Points: this paper describes how a ML pipeline should be run, which includes training, validation stages.

One-off pipeline:
Task-BAsed pipelne:

### Deep Learning Inference Service at Microsoft

[PDF Link](https://www.usenix.org/system/files/opml19papers-soifer.pdf)

1. Intelligent Model Placement: find the place suits model most
2. Low-Latency Model Execution: resource isolation and data locality & server-to-model communication
3. **Efficient Routing: Backup Requests** use a low-latency, less comlicated model as backup inference.

### Accelerating Large Scale Deep Learning Inference through DeepCPU at Microsoft

[PDF Link](https://www.usenix.org/system/files/opml19papers-zhang.pdf)

DeepCPu is a library for serving DL models

Scenario, Library and Technique

1. Major Deep Learning Scenarios
2. Highly Reusable Library
3. Performance Optimization Techniques

DeepCPU: C++ SDK

1. Customized optimization
2. Framework Integration: TF & ONNX

Comments: Intel OpenVINO may be better choice

### Towards Taming the Resource and Data Heterogeneity in Federated Learning

Nothing important

### KnowledgeNet: Disaggregated and Distributed Training and Serving of Deep Neural Networks

[PDF Link](https://www.usenix.org/system/files/opml19papers-biookaghazadeh.pdf)

KnowledgeNet (KN) disaggregates and distribute neural networks for both training and serving.

1. Split a large model into several small models, eah of which can be deployed on independent processing node.
2. Knowledge transfer technique in KN: transfer knowledge from large model from cloud to small model in edge device.

### MPP: Model Performance Predictor

[PDF Link](https://www.usenix.org/system/files/opml19papers-ghanta.pdf)

To predict the performance of a model (*that gonna be deployed*)

Error Dataset: Labels of this error dataset are the errors in predictions made by the
primary algorithm, and features could be a range of things depending on the application (* primary algorithm features themselves, predictions from the primary
algorithm, probability measures from the primary predictions or some algorithm-specific metrics, such as the number of trees or variation in output from different trees in a Random Forest*).

MPP algorithm focuses on predicting the performance of the primary algorithm.

We present MPP as a binary classification algorithm that predicts whether a prediction is correct (1) or incorrect (0).

### Katib: A Distributed General AutoML Platform on Kubernetes

[PDF Link](https://www.usenix.org/system/files/opml19papers-zhou.pdf)

### Disdat: Bundle Data Management for Machine Learning Pipelines

[PDF Link](https://www.usenix.org/system/files/opml19papers-yocum.pdf)

Not sure, nor that related.

Mentioned [Luigi](https://github.com/spotify/luigi) from Spotify.

### Low-latency Job Scheduling with Preemption for the Development of Deep Learning

[PDF Link](https://www.usenix.org/system/files/opml19papers-yabuuchi.pdf)

*TE: trial-and-error*
*BE: best-offort*

Comments: may be a nice suite for AutoML

Principle: prefer TE, preempt BE

1. Minimizing the re-scheduling intervals
2. Minimizing the number of preemptions
3. Minimizing the preemption-incurred time loss

### tensorflow-tracing: A Performance Tuning Framework for Production

[PDF Link](https://www.usenix.org/conference/opml19/presentation/hashemi)

*tensorflow-tracing*

1. Collecting application-level runtime metrics
2. Collecting low-oeverhead metrics automatically while expensive ones on demand
3. Standardize file format to exchange runtime metrics between users and admins


