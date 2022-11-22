# MLOps_Vertex_AI
MLOps를 위한 Vertex AI Tutorial 학습 및 실전적인 예제 적용까지를 목표로 합니다.

01_pipelines_intro_kfp Abstraction

1. Vertex AI에서의 Kubeflow Pipeline 사용 가능성
2. 초기 Project 세팅법
3. 앞으로 Docker Image를 활용한 각 Component별로 구체적인 구현 수행 필요


[20221122]
General Framework Pipeline 예제 분석 # 진행중
​https://blog.ml6.eu/a-general-framework-for-machine-learning-pipelines-on-gcp-b57e234f7d12?gi=e44724ff4877

1. kfp importer
2. TrainingJop, HyperparameterTuningJop, Results, ServingConfig 등 여러 Component들, GetTrainingArgsDictOp
3. 이어서 분석하여 전체적인 Component 구성 요소들의 이해 및 Dockerize를 통한 응용으로 이어지도록 할 예정
