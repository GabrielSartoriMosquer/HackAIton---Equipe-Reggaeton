graph TD;
    %% Definição de Estilos
    classDef pergunta fill:#e6f7ff,stroke:#0056b3,stroke-width:2px;
    classDef resposta fill:#f0f0f0,stroke:#555,stroke-width:1px;
    classDef produto fill:#d4edda,stroke:#155724,stroke-width:2px,font-weight:bold;

    %% NÓ RAIZ
    A(🤖 Qual sua necessidade principal?)
    class A pergunta;

    %% =============================================
    %% RAMO 1: SEGURANÇA (7 PRODUTOS)
    %% =============================================
    A --- B(👤 Proteger minha casa/negócio);
    B --> C(🤖 O que você busca?);
    
    %% Ramo 1.1: Câmeras Wi-Fi
    C --> D(👤 Câmeras Wi-Fi fáceis de instalar);
    D --> E(🤖 A câmera ficará em ambiente INTERNO ou EXTERNO?);
    E --> F(👤 Ambiente Interno);
    E --> G(👤 Ambiente Externo);
    F --> H(🤖 Você precisa que ela gire (360°)?);
    [cite_start]H --> P1(➡️ iMX C [cite: 2758]);
    [cite_start]H --> P2(➡️ iM4 C [cite: 2786]);
    G --> I(🤖 Você precisa que ela gire (360°)?);
    [cite_start]I --> P3(➡️ iM5 4 MP [cite: 2835]);
    [cite_start]I --> P4(➡️ iM7 S Full Color [cite: 2856]);

    %% Ramo 1.2: Fechaduras Digitais
    C --> J(👤 Fechaduras digitais para minha porta);
    J --> K(🤖 Como você prefere abrir a porta?);
    K --> L(👤 Apenas com Senha);
    K --> M(👤 Com Senha e Tag (Cartão));
    K --> N(👤 Com Biometria (Impressão Digital));
    [cite_start]L --> P5(➡️ FD 1000 [cite: 4214]);
    [cite_start]M --> P6(➡️ FD 2000 [cite: 4225]);
    [cite_start]N --> P7(➡️ FR 220 [cite: 4247]);
    
    %% Classes do Ramo Segurança
    class B,D,F,G,H,I,J,L,M,N resposta;
    class C,E,K pergunta;
    class P1,P2,P3,P4,P5,P6,P7 produto;


    %% =============================================
    %% RAMO 2: TI & REDES (7 PRODUTOS)
    %% =============================================
    A --- O(👤 Melhorar minha rede/internet);
    O --> P(🤖 Qual equipamento de rede você procura?);
    
    %% Ramo 2.1: Roteadores Residenciais
    P --> Q(👤 Roteador Wi-Fi para minha casa);
    Q --> R(🤖 Qual a velocidade da sua internet?);
    R --> S(👤 Até 70 Mega);
    R --> T(👤 100-400 Mega);
    R --> U(👤 Acima de 500 Mega);
    [cite_start]S --> P8(➡️ W4-300S [cite: 6311]);
    [cite_start]T --> P9(➡️ W5-1200GS [cite: 6311]);
    [cite_start]U --> P10(➡️ W6-1500 [cite: 6314]);

    %% Ramo 2.2: Roteadores/APs Empresariais
    P --> V(👤 Roteador Wi-Fi para meu negócio (PME));
    V --> W(🤖 O roteador ficará em ambiente INTERNO ou EXTERNO?);
    [cite_start]W --> P11(➡️ AP 310 [cite: 6319]);
    [cite_start]W --> P12(➡️ AP 1250 AC Outdoor [cite: 6322]);

    %% Ramo 2.3: Switches
    P --> X(👤 Switch para conectar equipamentos cabeados);
    X --> Y(🤖 Você precisa de PoE (energia pelo cabo) para câmeras ou telefones IP?);
    Y --> Z(👤 Não, apenas dados (Giga));
    Y --> AA(👤 Sim, preciso de PoE);
    [cite_start]Z --> P13(➡️ SG 800 Q+ [cite: 6329]);
    [cite_start]AA --> P14(➡️ SF 900 Hi-PoE [cite: 6329]);

    %% Classes do Ramo TI
    class O,Q,R,S,T,U,V,W,X,Y,Z,AA resposta;
    class P pergunta;
    class P8,P9,P10,P11,P12,P13,P14 produto;
    

    %% =============================================
    %% RAMO 3: ENERGIA (6 PRODUTOS)
    %% =============================================
    A --- BB(👤 Garantir energia ou automatizar);
    BB --> CC(🤖 Qual a sua necessidade?);
    
    %% Ramo 3.1: Nobreaks
    CC --> DD(👤 Proteger contra queda de energia (Nobreak));
    DD --> EE(🤖 O nobreak é para qual equipamento?);
    EE --> FF(👤 Computador / Videogame);
    EE --> GG(👤 Motor de Portão);
    FF --> HH(🤖 Setup Básico (1 PC) ou Avançado (Gamer)?);
    [cite_start]HH --> P15(➡️ ATTIV 600 [cite: 6546]);
    [cite_start]HH --> P16(➡️ ATTIV 1500 [cite: 6551]);
    GG --> II(🤖 Motor Comum ou Ultrarrápido (Senoidal)?);
    [cite_start]II --> P17(➡️ GNB 1000 [cite: 6563]);
    [cite_start]II --> P18(➡️ GNB 1500 PRO [cite: 6564]);

    %% Ramo 3.2: Casa Inteligente (Smart)
    CC --> JJ(👤 Automação / Casa Inteligente);
    JJ --> KK(🤖 O que você quer automatizar?);
    KK --> LL(👤 Lâmpadas (sem trocar o interruptor));
    KK --> MM(👤 Tomadas (Cafeteira, Ventilador));
    [cite_start]LL --> P19(➡️ EWS 211 (1 Tecla) [cite: 6648]);
    [cite_start]MM --> P20(➡️ EWS 301 (Tomada Smart) [cite: 6652]);
    
    %% Classes do Ramo Energia
    class BB,DD,EE,FF,GG,HH,II,JJ,KK,LL,MM resposta;
    class CC pergunta;
    class P15,P16,P17,P18,P19,P20 produto;