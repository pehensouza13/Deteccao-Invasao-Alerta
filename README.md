🔒 Detecção de Intrusos com IA e Alarme Sonoro
Este projeto utiliza Visão Computacional e Inteligência Artificial (IA) para detectar pessoas em tempo real em uma área específica de vigilância. Caso uma pessoa seja identificada dentro da área definida. A detecção é realizada utilizando o modelo YOLOv8n (You Only Look Once), uma das arquiteturas mais rápidas e eficientes para detecção de objetos.

📸 Demonstração
A imagem e os vídeos incluídos mostram o funcionamento do sistema em ação, onde uma pessoa entrando na área restrita dispara o alerta visual.

🧠 Tecnologias Utilizadas
Python — linguagem de programação principal.

OpenCV — captura e manipulação de vídeo e imagens.

YOLOv8 (Ultralytics) — modelo de IA para detecção de objetos.

🛠️ Instalação e Execução
Pré-requisitos
Python 3.8+


Instale as dependências:
bash
Copiar
Editar
pip install opencv-python ultralytics
Certifique-se também de ter o modelo YOLOv8 (yolov8n.pt) salvo no mesmo diretório do script.

Execute o projeto:
bash
Copiar
Editar
python main.py

📂 Estrutura do Projeto
bash
Copiar
Editar
├── main.py             # Script principal
├── yolov8n.pt          # Modelo pré-treinado YOLOv8n
├── ex02.mp4            # Vídeo de entrada (câmera simulada)
├── img01.png           # Imagem de exemplo de detecção

🤖 Técnica de IA Utilizada
YOLOv8 - You Only Look Once
YOLOv8 é uma arquitetura de detecção de objetos baseada em deep learning, projetada para identificar múltiplos objetos em uma imagem com alta velocidade e precisão. No projeto:

Utiliza-se o modelo YOLOv8n, uma versão leve ideal para aplicações em tempo real.

A IA é capaz de identificar o objeto pessoa (classe 0 no COCO dataset).

As coordenadas da caixa delimitadora (bounding box) são analisadas para verificar se o centro do objeto está dentro da área de risco.

Detecção de Intrusão
A área monitorada é definida como um retângulo no vídeo:

python
Copiar
Editar
area = [100,190, 1150,700]
Se o centro de uma pessoa detectada estiver dentro dessa área, o sistema:

Mostra alerta visual na tela.


🔔 Funcionalidades
Detecção em tempo real de pessoas.

Definição de uma zona sensível.

Alerta visual (overlay vermelho + mensagem).
