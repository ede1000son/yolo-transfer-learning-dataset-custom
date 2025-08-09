# Detecção de Equipamentos de Segurança com YOLOv11

![Licença](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.9-blue.svg)
![Framework](https://img.shields.io/badge/framework-YOLOv11-orange.svg)
![Feito com](https://img.shields.io/badge/feito%20com-Anaconda-green.svg)

Este repositório contém um projeto completo de visão computacional para treinar um modelo **YOLOv11** a detectar objetos personalizados. Utilizando a técnica de **Transfer Learning**, o modelo foi especializado para identificar equipamentos de segurança, especificamente **capacetes** e **extintores**.

O projeto foi desenvolvido para demonstrar o fluxo de trabalho completo: desde a criação e organização de um dataset, passando pelo treinamento e aumento de dados, até a análise de performance do modelo final.

## 🚀 Resultados do Treinamento

O modelo foi treinado por 100 épocas, demonstrando um aprendizado saudável e atingindo excelentes métricas de performance. Os gráficos abaixo resumem a evolução do treinamento, mostrando a queda das perdas e o aumento da precisão do modelo.

![Gráficos de Resultado do Treinamento](https://github.com/ede1000son/yolo-transfer-learning-dataset-custom/blob/main/results.jpg)

## 📂 Estrutura do Repositório

```
yolo-transfer-learning-dataset-custom/
│
├── dataset/                    # Contém o dataset personalizado
│   ├── train/
│   │   ├── images/
│   │   └── labels/
│   └── val/
│       ├── images/
│       └── labels/
│
├── runs/                       # Pasta gerada pelo YOLO com os resultados
│   └── detect/
│       └── train.../
│           ├── weights/        # Contém os pesos do modelo (best.pt, last.pt)
│           └── results.jpg     # Gráficos de resultado
│
├── dataset.yaml                # Arquivo de configuração do dataset
├── results.jpg                 # Cópia dos resultados para fácil visualização
└── yolo_transfer_learning_dataset_custom.ipynb   # O notebook principal com todo o código
```

## ⚙️ Configuração do Ambiente e Instalação

Este projeto foi testado no **Windows 11 Pro (Versão 24H2)** e também é compatível com distribuições **Linux**. Recomenda-se o uso do Anaconda para gerenciar o ambiente virtual.

### Pré-requisitos
- **Git:** Para clonar o repositório.
- **Anaconda ou Miniconda:** Para criar o ambiente virtual e instalar as dependências.

### Guia Passo a Passo

1. **Clone o repositório:**
   Abra um terminal (ou Anaconda Prompt) e execute o comando abaixo:
   ```bash
   git clone https://github.com/ede1000son/yolo-transfer-learning-dataset-custom.git
   cd yolo-transfer-learning-dataset-custom
   ```

2. **Crie um ambiente virtual com Conda:**
   Vamos criar um ambiente chamado `yolo_env` com a versão específica do Python.
   ```bash
   conda create --name yolo_env python=3.9.23
   ```

3. **Ative o ambiente recém-criado:**
   ```bash
   conda activate yolo_env
   ```

4. **Instale o pacote `ultralytics`:**
   A biblioteca `ultralytics` contém o YOLOv11 e todas as dependências necessárias (como PyTorch). A instalação é simples:
   ```bash
   pip install ultralytics
   ```

## ▶️ Como Executar o Projeto

Com o ambiente configurado e ativado, você está pronto para rodar o projeto.

1. **Inicie o Jupyter Notebook:**
   No seu terminal, dentro da pasta do projeto, execute:
   ```bash
   jupyter notebook
   ```

2. **Abra e execute o notebook:**
   Seu navegador abrirá uma nova aba. Clique no arquivo `yolo_transfer_learning_dataset_custom.ipynb` para abri-lo. Você pode executar todas as células sequencialmente para replicar o processo de treinamento e análise.

## 🎨 Usando Seu Próprio Dataset

Este projeto foi pensado para ser facilmente adaptável a outros datasets.

1. **Rotulagem das Imagens:**
   - Todas as imagens utilizadas neste projeto foram obtidas sob a licença **Creative Commons**.
   - Para rotular suas próprias imagens, recomenda-se o aplicativo [**AnyLabeling**](https://anylabeling.nrl.ai/). Ele é intuitivo e exporta diretamente para o formato YOLO (.txt).

2. **Organização das Pastas:**
   - Adicione suas imagens e arquivos de anotação na pasta `dataset/`, respeitando a estrutura `train/images`, `train/labels`, `val/images` e `val/labels`.

3. **Configuração do Dataset:**
   - Abra o arquivo `dataset.yaml` e altere o número e os nomes das classes para que correspondam aos seus novos objetos.

4. **Predição:**
   - Lembre-se que, ao alterar o dataset de treinamento, você também deverá alterar as imagens utilizadas para a predição no final do notebook para que sejam relevantes para suas novas classes.

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](https://github.com/ede1000son/yolo-transfer-learning-dataset-custom/blob/main/LICENSE) para mais detalhes.