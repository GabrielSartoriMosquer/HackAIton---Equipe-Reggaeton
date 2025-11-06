# Hackathon - Árvore de Decisão Intelbras

Este é o fluxograma visual do nosso chatbot para o MVP.

## Fluxo Principal

\`\`\`mermaid
graph TD;
    %% Definição de Estilos
    classDef pergunta fill:#e6f7ff,stroke:#0056b3,stroke-width:2px;
    classDef resposta fill:#f0f0f0,stroke:#555,stroke-width:1px;
    classDef produto fill:#d4edda,stroke:#155724,stroke-width:2px,font-weight:bold;

    %% NÓ RAIZ
    A(🤖 Qual sua necessidade principal?)
    class A pergunta;

    %% =============================================
    %% RAMO 1: SEGURANÇA
    %% =============================================
    A --- B(👤 Proteger minha casa/negócio);
    B --> C(🤖 O que você busca?);
    
    %% Ramo 1.1: Câmeras
    C --> D(👤 Monitorar com câmeras);
    D --> E(🤖 Wi-Fi ou Cabeada?);
    E --> F(👤 Prefiro simples, Wi-Fi);
    F --> G(🤖 Ambiente Interno ou Externo?);
    
    %% Ramo 1.1.1: Câmeras Internas
    G --> H(👤 Interno);
    H --> I(🤖 Câmera Fixa ou 360°?);
    I --> J(👤 Fixa é suficiente);
    I --> K(👤 Preciso que gire 360°);
    J --> P1(➡️ iMX C / iMX1);
    K --> P2(➡️ iM4 C);
    
    %% Ramo 1.1.2: Câmeras Externas
    G --> L(👤 Externo);
    L --> M(🤖 Zoom/360° ou Fixa?);
    M --> N(👤 Preciso de Zoom e 360°);
    M --> O(👤 Apenas câmera fixa);
    N --> P3(➡️ iM7+ Zoom);
    O --> P4(➡️ iM5 4 MP);

    %% Ramo 1.2: Controle de Acesso (Fechaduras)
    C --> AC_D(👤 Controlar quem entra e sai);
    AC_D --> AC_E(🤖 Como gostaria de abrir a porta?);
    AC_E --> AC_F(👤 Apenas com Senha);
    AC_E --> AC_G(👤 Com Senha e Tag/Cartão);
    AC_E --> AC_H(👤 Com Biometria (Digital));
    AC_F --> P_AC1(➡️ FD 1000);
    AC_G --> P_AC2(➡️ FD 2000 / FD 3000);
    AC_H --> P_AC3(➡️ FR 220 / FR 331);
    
    %% Classes do Ramo Segurança
    class B,D,F,H,J,K,L,N,O,AC_D,AC_F,AC_G,AC_H resposta;
    class C,E,G,I,M,AC_E pergunta;
    class P1,P2,P3,P4,P_AC1,P_AC2,P_AC3 produto;


    %% =============================================
    %% RAMO 2: TECNOLOGIA DA INFORMAÇÃO (TI)
    %% =============================================
    A --- IT_B(👤 Melhorar minha rede/internet);
    IT_B --> IT_C(🤖 Qual equipamento de rede?);
    IT_C --> IT_D(👤 Roteador Wi-Fi para casa);
    IT_D --> IT_E(🤖 Qual a velocidade da sua internet?);
    
    %% Ramos de Velocidade
    IT_E --> IT_F(👤 Até 70 Mega);
    IT_F --> P_IT1(➡️ W4-300S);
    
    IT_E --> IT_G(👤 100-400 Mega);
    IT_G --> P_IT2(➡️ W5-1200GS);
    
    IT_E --> IT_H(👤 Acima de 500 Mega);
    IT_H --> P_IT3(➡️ W6-1500 / RX 3000);

    %% Classes do Ramo TI
    class IT_B,IT_D,IT_F,IT_G,IT_H resposta;
    class IT_C,IT_E pergunta;
    class P_IT1,P_IT2,P_IT3 produto;
    

    %% =============================================
    %% RAMO 3: ENERGIA
    %% =============================================
    A --- EN_B(👤 Gerar ou garantir energia);
    EN_B --> EN_C(🤖 Qual a sua necessidade?);
    EN_C --> EN_D(👤 Proteger contra queda de energia (Nobreak));
    EN_D --> EN_E(🤖 É para qual tipo de uso?);

    %% Ramo 3.1.1: Nobreaks Residenciais
    EN_E --> EN_F(👤 Computador/TV/Videogame);
    EN_F --> EN_G(🤖 Setup simples (1 PC) ou setup maior (Gamer)?);
    EN_G --> EN_H(👤 Setup Simples);
    EN_H --> P_EN1(➡️ ATTIV 600 / XNB 600);
    EN_G --> EN_I(👤 Setup Maior / Gamer);
    I --> P_EN2(➡️ ATTIV 1200 / ATTIV 1500);

    %% Ramo 3.1.2: Nobreaks para Portão
    EN_E --> EN_J(👤 Motor de portão automático);
    EN_J --> EN_K(🤖 Motor comum ou ultrarrápido?);
    EN_K --> EN_L(👤 Motor comum (até 1/2 HP));
    L --> P_EN3(➡️ GNB 1000);
    EN_K --> EN_M(👤 Motor ultrarrápido (placa inversora));
    M --> P_EN4(➡️ GNB 1500 PRO);
    
    %% Classes do Ramo Energia
    class EN_B,EN_D,EN_F,EN_G,EN_H,EN_I,EN_J,EN_K,EN_L,EN_M resposta;
    class EN_C,EN_E,EN_K pergunta;
    class P_EN1,P_EN2,P_EN3,P_EN4 produto;
\`\`\`