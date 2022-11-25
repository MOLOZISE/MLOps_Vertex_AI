# MLOps_Vertex_AI
MLOps를 위한 Vertex AI Tutorial 학습 및 실전적인 예제 적용까지를 목표로 합니다.

[20221121]
01_pipelines_intro_kfp Abstraction

1. Vertex AI에서의 Kubeflow Pipeline 사용 가능성
2. 초기 Project 세팅법
3. 앞으로 Docker Image를 활용한 각 Component별로 구체적인 구현 수행 필요


[20221122]
General Framework Pipeline 예제 분석 # 진행중
https://blog.ml6.eu/a-general-framework-for-machine-learning-pipelines-on-gcp-b57e234f7d12?gi=e44724ff4877

1. kfp importer
2. TrainingJop, HyperparameterTuningJop, Results, ServingConfig 등 여러 Component들, GetTrainingArgsDictOp
3. 이어서 분석하여 전체적인 Component 구성 요소들의 이해 및 Dockerize를 통한 응용으로 이어지도록 할 예정

[20221123]
https://blog.ml6.eu/a-general-framework-for-machine-learning-pipelines-on-gcp-b57e234f7d12?gi=e44724ff4877

1. Google Colab 전반적인 분석
2. Train Component는 Dockerfile로, 나머지 Component들은 Local function으로 정의함, 특히 여러 Component들의 연결성을 고려하여 설계한 것이 인상 깊음
3. 실제 프로젝트에 적용할 때에는, Dockerization을 위한 Component들을 ML Workflow에서 주요 핵심 부분들만을 선정하여 결정하고, 나머지는 Local function으로 정의하는 방향으로 설계하는 것이 바람직하다고 생각함. 그리고, GCP Cloud Bucket, Registry와 연결하는 부분을 적극 활용하여 프로젝트에 적용할 수 있도록 해야함.

[20221124 - 20221125]
https://blog.ml6.eu/a-general-framework-for-machine-learning-pipelines-on-gcp-b57e234f7d12?gi=e44724ff4877

1. Google Colab : project setting, Dockerfile build & push, Pipeline specification & run 수행 확인
2. Component : 각 컴포넌트들의 깊은 이해 및 AutoML Container와의 결합 찾기
3. Total Flow : Data Load -> Data Preprocess -> Hyperparameter_tuning(Model_train, Model_evaluation, AutoML) -> Deployment Process
보다 자세한 Component 분석은 pdf 참고
