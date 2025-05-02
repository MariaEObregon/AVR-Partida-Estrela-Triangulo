# ⭐🔺 Partida Estrela Triângulo com AVR e Arduino
Este projeto consiste no desenvolvimento de um circuito com programação em AVR para controlar uma aplicação de um dispositivo de comando para partida Estrela-Triângulo. O funcionamento é o seguinte:

Quanto S1 é pressionado, ocorre o fechamento do comando em estrela(contatores K1 e K2), e após 5 segundo, o fechamento do comando elétrico passa a ser triângulo(contatores K1 e K3).
A qualquer momento, quando apertato o botão S0, o circuito é interrompido.

🛠 Tecnologias e Componentes Utilizados:

| Componente            | Modelo                                                                                                                               | Descrição                                                                                                                                     |
| :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| Microcontrolador      | [AVR - ATMega328P](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-7810-Automotive-Microcontrollers-ATmega328P_Datasheet.pdf) | Plataforma Arduino Uno como interface                                                                                                         |
| IDE                   | [MPLabX](https://www.microchip.com/en-us/tools-resources/develop/mplab-x-ide)                                                        | Ambiente de Desenvolvimento Integrado - [Instalação](https://developerhelp.microchip.com/xwiki/bin/view/software-tools/ides/x/install-guide/) |
| Compilador            | [XC8](https://www.microchip.com/en-us/tools-resources/develop/mplab-xc-compilers/xc8)                                                | [Instalação](https://developerhelp.microchip.com/xwiki/bin/view/software-tools/xc8/install/)                                                  |
| Editor de código      | [Visual Studio Code](https://code.visualstudio.com/)                                                                                | [v1.97.2](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user)                         |
| Construtor de projeto | [Makefile](https://stackoverflow.com/questions/32127524/how-to-install-and-use-make-in-windows)                                      | Power Shell<br>`winget install Chocolatey.Chocolatey`<br>`choco install make`                                                                 |
| Gravador do AVR       | [AVRDudess](https://github.com/ZakKemble/AVRDUDESS/releases/tag/v2.18)                                                               | [ZakKemble/AVRDUDESS/v2.18](https://github.com/ZakKemble/AVRDUDESS/releases/download/v2.18/AVRDUDESS-2.18-setup.exe)                          |
| Simulador eletrônico  | [SimulIDE](https://simulide.com/p/downloads/)                                                                                        | Power Shell<br>`winget install SimulIDE.SimulIDE`                                                                                             |
| Versionamento         | [git](https://git-scm.com/downloads)                                                                                                 | Power Shell<br>`winget install --id Git.Git -e --source winget`                                                                               |

Este projeto faz parte de uma atividade acadêmica e tem como objetivo a aplicação prática de conceitos de eletrônica e programação embarcada.

🗺️ Mapa de entradas e saídas:

| Função  | Dispositivo   | Descrição                         | Pino (Arduino Uno) | Pino (ATmega328P) | PORT |
| :------ | :------------ | :-------------------------------- | :----------------- | :-----------------|:-----|
| Entrada | Botão S0      | Desliga sistema de comando       | 9                  | 15                | PB1  |
| Entrada | Botão S1      | Liga sistema de comando          | 10                 | 16                | PB2  |
| Saída   | K3            | Contator K3                       | 11                 | 17                | PB3  |
| Saída   | K2            | Contator K2                       | 12                 | 18                | PB4  |
| Saída   | K1            | Contator K1                       | 13                 | 19                | PB5  |


| ⭐🔺 Simulação no SimulIDE: |
|:----------------------------------------------------------------:|
| ![EstrelaTriangulo](EstrelaTriangulo.gif)                                   |
