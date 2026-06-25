# Detecção e Classificação de Objetos Astronômicos com YOLO

Este repositório contém o código-fonte e as configurações desenvolvidas para o projeto de  focado na detecção, localização e classificação automatizada de galáxias e outros objetos astronômicos, utilizando modelos da família YOLO (You Only Look Once).

O projeto aplica técnicas de Deep Learning e Visão Computacional sobre dados de imagens multiespectrais provenientes do Legacy Survey (DR10).

---

## Tecnologias e Dependências 


###  Dependências Principais do Sistema (Python & Core ML)
* **Python 3.10+**: Base de execução do ecossistema.
* **Ultralytics **: Framework de Visão Computacional utilizado para a arquitetura de detecção, cálculo de bounding boxes e otimização de pesos.
* **PyTorch (com suporte a CUDA)**: Backend de Deep Learning. Essencial para alocação dos tensores e processamento das camadas convolucionais diretamente nos núcleos da GPU.

### Dependências Científicas e de Processamento de Dados
* **Astropy**: Biblioteca fundamental para a astronomia em Python. Utilizada para ler metadados astronômicos, converter sistemas de coordenadas celestes (RA/DEC) e manipular arquivos em formato astronômico (FITS/TIFF astronômicos).
* **NumPy & Pandas**: Manipulação matricial fina das imagens tratadas como tensores e estruturação dos dados tabulares de objetos.
* **OpenCV (cv2) & Pillow (PIL)**: Leitura de imagens multiespectrais do Legacy Survey, redimensionamento de canais e transformações geométricas para o pipeline de dados do YOLO.
* **Matplotlib & Seaborn**: Geração de gráficos de perda (loss), curvas de Precisão-Revocação (PR Curve) e visualização de matrizes de confusão morfológica.

---


##  Estrutura do Repositório

```text
├── data_processing.ipynb       # Pipeline de preparação, corte e aumento de dados astronômicos
├── get_data_datalab.ipynb      # Notebook para extração e download das imagens do Legacy Survey
├── train.ipynb                 # Notebook de testes, análises e visualização do treinamento
├── galaxy_data.yaml            # Arquivo de configuração de classes e caminhos para o YOLO
├── environment.yml             # Arquivo de dependências para recriar o ambiente Conda
