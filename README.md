# Kimauánisso - GitHub

Cada robô possui seu proprio repositorio, e todos seguem a mesma estrutura, que está descrita abaixo:

```
nome_do_robo/
├── README.md
├── .gitignore
├── src/
│   ├── aruivos_auxiliares.cpp
├── include/
│   └── arquivos_auxiliares.h
└── nome_do_robo.c
```

---
## Como criar um novo projeto?
Para criar um novo projeto, abra o Visual Studio Code 
<img src="https://code.visualstudio.com/assets/images/code-stable.png" alt="VS Code Logo" width="20" style="vertical-align: middle;"/> 
e clique no icone 
<img src="arquivos_auxiliares\icone_ext_pico.png" alt="Extensão Pico" width="32" style="vertical-align: middle;"/>.

Caso o icone não exista, é necessario instalar a extensão da Raspberry Pi Pico, para isso, abra a aba de extensões e pesquise por *Raspberry Pi Pico*, a primeira extensão que aparecer é a que você deve instalar.

Na barra lateral, aparecerá um menu, clique na opção *New C/C++ Project*:

<img src="arquivos_auxiliares\ext_pico_parte1.png" alt="Barra Lateral Extensão Pico" />

Na janela que foi aberta, configure os campos indicados com a seta:

<img src="arquivos_auxiliares\ext_pico_parte2.png" alt="Criação do Projeto" />

- Name: nome do projeto, quse sempre será o nome do robô
- Board Type: qual placa de desenvolvimento está sendo usada, as opções mas comuns são:
  - Pico -> Raspberry Pi Pico padrão
  - Pico W -> Raspberry Pi Pico com suporte para Wi-Fi e Bluetooth
  - Other -> Outras placas que utilizem os microcontroladores da Raspberry Pi Foundation (RP2040 e RP235X), como por exemplo: Waveshare RP2040 Zero
- Location: onde você quer salvar o projeto
- Generate C++ code: habilitar essa opção para gerar o arquivo principal com a extensão .cpp

Caso tenha selecionado *Other* no Board Type, um menu com varias opções de placas aparecerá, escolha aquela que está sendo utilizada.

Após um tempo, uma nova instancia do VS Code será aberta, nela estará seu projeto.

---
## Como compilar e passar o programa pra o microcontrolador?

Quando o arquivo estiver pronto para ser compilado e colocado no robô, basta voltar ao menu lateral usado para criar o projeto e clicar no botão *Compile Project*, isso irá gerar o arquivo necessário para programar o microcontrolador.

Quando o projeto terminar de ser compilado, abra a pasta *build/* no explorador de arquivos e procure pelo arquivo *nome_do_robo.uf2*.

<img src="arquivos_auxiliares\explorador_de_arquivos.png" alt="Diretório build/" />

Agora conecte o robô no computador enquanto pressiona o botão *BOOTSEL* na placa do microcontrolador, isso irá fazer com que o MCU apareça no modo de *mass storage*, permitindo que ele seja visto no explorador de arquivos. Agora basta copiar o arquivo .uf2 e colar dentro do armazenamento do microcontrolador.

[mostrando como copiar e colar para pico]