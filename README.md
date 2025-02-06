# Tutorial: Intel® Galileo – Do Básico à Configuração (Gen 1 vs Gen 2)

![Intel Galileo Logo](https://embarcados.com.br/wp-content/uploads/2014/03/imagem-de-destaque-12.png.webp)

Este tutorial apresenta a placa Intel® Galileo – uma plataforma de desenvolvimento Arduino‑certificada baseada no processador Intel® Quark™ SoC X1000 – abordando:

- **Objetivo e aplicações**
- **Comparação entre Gen 1 e Gen 2**
- **Estrutura e diagramas**
- **Funcionalidades e recursos**
- **Configuração e instalação de um sistema operacional**
- **Importância na cibersegurança**

---

## 1. Descrição Geral

A placa **Intel® Galileo** foi desenvolvida para facilitar a prototipação e os projetos educacionais, integrando a familiaridade do ambiente Arduino com o desempenho dos processadores Intel. Seus principais objetivos são:

- **Compatibilidade com Shields Arduino:**  
  Expansão de funcionalidades utilizando shields projetados para o Arduino Uno R3.
- **Execução de Sistemas Operacionais Linux:**  
  Permite rodar distribuições Linux (baseadas em Yocto), ampliando as possibilidades de aplicação em IoT e projetos profissionais.
- **Flexibilidade de Programação:**  
  Programável via Arduino IDE e compatível com diversas linguagens.
- **Aplicações em IoT e Educação:**  
  Ideal para makers, educadores e desenvolvedores que buscam um ambiente de baixo custo e alta versatilidade.

---

## 2. Comparação: Gen 1 vs Gen 2

A Intel® Galileo foi lançada em duas gerações. A tabela a seguir destaca as principais diferenças:

| **Característica**                | **Gen 1**                                | **Gen 2**                                                      |
|-----------------------------------|------------------------------------------|----------------------------------------------------------------|
| **Processador (SoC)**             | Intel® Quark™ X1000 32-bit, 400 MHz       | Intel® Quark™ X1000 32-bit, 400 MHz                             |
| **Alimentação (Barrel Jack)**     | 5V (via USB e fonte externa)             | Aceita de 7V a 15V – maior flexibilidade com opção PoE*         |
| **Console Serial**                | RS‑232 (jack de áudio)                    | Cabeçalho de 6 pinos USB TTL (3,3V), compatível com FTDI         |
| **PWM**                           | Resolução limitada                        | 6 canais PWM de 12 bits para controle mais preciso              |
| **Redirecionamento de UART**      | Não disponível                           | UART pode ser redirecionado para os headers Arduino             |
| **Preço (na época)**              | Aproximadamente US$70                     | Geralmente um pouco mais elevado (US$80 a US$100, dependendo do mercado) |

*Os preços e condições podem variar conforme o mercado e a disponibilidade.  
[Ver referências](#referências)

---

## 3. Estrutura da Placa

A Intel® Galileo integra elementos de um microcontrolador e de um computador de placa única (SBC). Seus componentes principais incluem:

- **Processador:** Intel® Quark™ X1000, 400 MHz  
- **Memória:**  
  - 256 MB DDR3  
  - 512 KB SRAM embarcada  
  - 8 MB NOR Flash  
  - 8 KB EEPROM  
- **Interfaces de I/O:**  
  - 20 pinos digitais (12 com alta velocidade)  
  - 6 entradas analógicas  
  - 6 canais PWM de 12 bits (na Gen 2)  
  - 2 UARTs (com redirecionamento na Gen 2)  
  - Interfaces I²C, SPI e ICSP  
- **Conectores e Expansões:**  
  - Header compatível com Arduino Uno R3  
  - Conector Ethernet 10/100 com suporte PoE (na Gen 2)  
  - Slot para cartão microSD (até 32 GB)  
  - Portas USB: USB Host (Type A) e USB Client (micro-USB)  
  - Cabeçalho para console serial via USB TTL  
  - Slot mini-PCI Express para módulos adicionais

---

## 4. Galeria de Imagens

### Intel® Galileo Gen 1
![Intel Galileo Gen 1](https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Embedded_World_2014_Intel_Galileo_01.jpg/330px-Embedded_World_2014_Intel_Galileo_01.jpg)  
*Imagem ilustrativa da placa Intel® Galileo Gen 1 (fonte: Wikipedia)*

### Intel® Galileo Gen 2
![Intel Galileo Gen 2](https://www.mouser.do/images/microsites/galileo-2-raspberry-pi-2-fig-1.png)  
*Imagem ilustrativa da placa Intel® Galileo Gen 2 (fonte: Botnroll)*

---

## 5. Diagramas

Para detalhes completos do hardware, consulte os documentos oficiais:

- **Diagrama de Bloco e Esquemáticos:**  
  ![Diagrama de bloco](https://github.com/facens-cybersec/galileo-challenge/blob/main/imagens/diagramadeblocos.png?raw=true)

- **Layout dos Headers Arduino:**  
  A disposição dos pinos segue o padrão do Arduino Uno R3, facilitando a integração com shields.  
  ![Header Arduino Compatível](https://raw.githubusercontent.com/arduino/Arduino/main/build/shared/arduino_uno_r3_header.png)

---

## 6. Funcionalidades e Recursos

A Galileo Gen 2 oferece diversos recursos que a diferenciam:

- **Compatibilidade Arduino:**  
  Programável com o Arduino IDE e compatível com shields Arduino.
- **Desempenho Superior:**  
  Processador de 400 MHz com 256 MB de memória DDR3, muito mais robusto que os microcontroladores tradicionais.
- **Interfaces de Expansão Industriais:**  
  Conectores Ethernet, USB, microSD e mini-PCI Express ampliam as possibilidades de aplicação.
- **PWM de Alta Resolução:**  
  Controle preciso para aplicações de servos e motores.
- **Flexibilidade de Alimentação:**  
  Aceita fontes de 7V a 15V e suporta Power-over-Ethernet (PoE).
- **Sistema Operacional Linux:**  
  Possui uma imagem Linux baseada em Yocto, que pode ser personalizada e atualizada.
- **Expansibilidade:**  
  Slot mini-PCI Express permite a integração de módulos WiFi, Bluetooth, entre outros.

---

## 7. Configuração da Placa

2. **Arduino IDE:**  
   - Abra o Arduino IDE.
   - Vá em **Ferramentas → Placa** e selecione **Intel® Galileo Gen 2**.
   - Escolha a porta serial correspondente.
   - Carregue um exemplo simples, como o **Blink**, para testar a comunicação.

### 7.3 Configuração de Energia e Conexões

- **Alimentação:**  
  Utilize uma fonte adequada (7V–15V para a Gen 2) e conecte o cabo USB para programação e debug.
- **Rede:**  
  Conecte um cabo Ethernet ou módulos WiFi via slot mini-PCI Express para habilitar conectividade.
- **Armazenamento:**  
  Insira um cartão microSD (FAT32, até 32GB) para armazenamento persistente.

---

## 8. Instalação de um Sistema Operacional

### Passos Básicos:

1. **Download da Imagem:**  
   Baixe a imagem Linux Alpine (“sdcard.alpine.img.gz”) do Galileu Resurection https://github.com/dmarkey/galileo-resurrection e extraia para uma pasta.
   Ele já vem com o gerenciador de pacotes funcionando e o SSH configurado.

   ![image](https://github.com/user-attachments/assets/ae4829f6-7a11-4069-bb82-6580f9f2f8c7)


3. **Preparação do Cartão microSD:**  
   Formate o cartão em FAT32 e utilize uma ferramenta (Win32 Disk Imager) para gravar a imagem.
  
   
5. **Gravação da Imagem:**  
   Siga as instruções da ferramenta para gravar a imagem no cartão e aguarde a conclusão.

   Basta selecionar o device com o MicroSD, selecionar a imagem (“sdcard-alpine.img”) em “image file” e clicar em Write.

    ![image](https://github.com/user-attachments/assets/e8b5ba69-104b-456a-bff8-9c212346e500)


7. **Boot:**  
   Insira o cartão na placa, conecte a fonte e o cabo USB. A placa fará boot a partir do cartão, carregando o sistema operacional.

8. **Verificação:**  
   Use SSH (através do endereço IP atribuído pelo seu roteador) para acessar o terminal e confirmar a instalação.

   Voce pode utilizar o software Advanced IP Scanner para procurar o IP da placa Galileo, ou se preferir pode utilizar o comando "ipconfig" no Windows PowerShell.

   ![image](https://github.com/user-attachments/assets/35749222-477f-4261-9fdc-0ba424b489ec)

   
   Após identificar o IP, acesse o sistema via SSH, utilizando o software PuTTY, coloque o ip da placa Galileo em host name e depois Open.
   
   ![image](https://github.com/user-attachments/assets/7149156f-fac1-4caf-8dc9-e4a679b737ef)

   As credenciais padrão são (galileo/galileo ou root/root).

   ![image](https://github.com/user-attachments/assets/5989b327-a2e6-4bad-b400-5ebd04399fac)
   


---

## 9. Conclusão: Importância para a Cibersegurança

Estudar a Intel® Galileo é essencial para:

- **Entender a Integração Hardware-Software:**  
  Permite identificar pontos vulneráveis nas interfaces (USB, Ethernet, mini-PCI Express) e reforçar a segurança.
- **Desenvolver Soluções IoT Seguras:**  
  Projetar dispositivos IoT seguros com *security by design* utilizando plataformas híbridas que combinam microcontroladores e sistemas operacionais robustos.
- **Gerenciamento do Ciclo de Vida:**  
  Discutir a importância das atualizações e do gerenciamento do ciclo de vida dos dispositivos, evitando vulnerabilidades decorrentes de firmware desatualizado.

---

## Referências

- **Intel® Galileo Gen 2 Datasheet**  
  [Intel Galileo Gen 2 Datasheet PDF](https://www.intel.com/content/dam/www/public/us/en/documents/datasheets/galileo-g2-datasheet.pdf)  
 

- **Intel Galileo – Wikipedia**  
  [Intel Galileo - Wikipedia](https://en.wikipedia.org/wiki/Intel_Galileo)  


- **Getting Started with Intel® Galileo Gen2**  
  [Arduino Documentation: Galileo](https://www.arduino.cc/en/Guide/IntelGalileoGen2)  

