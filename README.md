# 🛡️ Emotional Shield COBOL  
### *A Lightweight Emotional Processing Engine in Pseudo-COBOL*

## 📌 Sobre o Projeto

**Emotional Shield COBOL** é um projeto simbólico e experimental que utiliza pseudo-COBOL para representar a lógica de um **filtro emocional interno** — um sistema capaz de:

- analisar eventos ou frases recebidas,
- detetar gatilhos emocionais,
- calcular carga emocional,
- e devolver uma resposta regulada, estruturada e segura.

É um exercício de **engenharia emocional**, **metáfora computacional** e **criatividade técnica**, transformando sentimentos complexos em lógica clara, determinística e auditável.

---

## 🎯 Objetivos do Projeto

- Criar uma abordagem estruturada para representar processos emocionais.
- Explorar como conceitos de programação podem ajudar na autorregulação e na compreensão do impacto emocional.
- Permitir que outras pessoas criem os seus próprios “módulos de escudo” personalizáveis.
- Demonstrar que mesmo linguagens rígidas como COBOL podem ser utilizadas metaforicamente para domínios humanos e subjetivos.

---

## 📁 Estrutura do Repositório

```
emotional-shield-cobol/
│
├── src/
│   ├── emotional_shield_generic.cob
│   ├── emotional_shield_extended.cob
│   ├── emotional_shield_debug.cob
│   └── emotional_shield_event_samples.cob
│
├── docs/
│   ├── architecture_diagram.png
│   └── emotional_flowchart.png
│
├── examples/
│   ├── input_samples.txt
│   └── expected_outputs.txt
│
└── README.md
```

---

## 🧠 Arquitetura Emocional

O “motor emocional” segue quatro passos:

1. **Receção do evento**  
2. **Análise de gatilhos**  
3. **Cálculo da carga total**  
4. **Geração da resposta**  

---

## 🧩 Como Funciona (Pseudo-COBOL)

### Entrada  
```
"Porque fizeste isto outra vez?"
```

### Processamento  
- Deteta “CRÍTICA”
- Soma carga emocional
- Compara com thresholds

### Saída  
```
"REGISTAR EVENTO SEM INTERNALIZAR."
```

---

## 🛠 Exemplos de Código

```cobol
       IDENTIFICATION DIVISION.
       PROGRAM-ID. EMOTIONAL-SHIELD.

       DATA DIVISION.
       WORKING-STORAGE SECTION.

       01 INPUT-EVENT     PIC X(200).
       01 EMOTIONAL-LOAD  PIC 9(03) VALUE 0.
       01 RESPONSE        PIC X(200).

       01 TRIGGERS.
          05 WORD PIC X(20) OCCURS 5 TIMES
             VALUE "CRITICA",
                   "ATAQUE",
                   "CULPA",
                   "AGRESSIVIDADE",
                   "DESVALORIZACAO".

       PROCEDURE DIVISION.
           ACCEPT INPUT-EVENT.

           PERFORM VARYING IDX FROM 1 BY 1 UNTIL IDX > 5
              IF INPUT-EVENT CONTAINS WORD(IDX)
                 ADD 20 TO EMOTIONAL-LOAD
              END-IF
           END-PERFORM.

           IF EMOTIONAL-LOAD > 60
              MOVE "EVENTO BLOQUEADO." TO RESPONSE
           ELSE IF EMOTIONAL-LOAD > 20
              MOVE "APLICAR AUTOCUIDADO." TO RESPONSE
           ELSE
              MOVE "PROCESSAMENTO NEUTRO." TO RESPONSE
           END-IF.

           DISPLAY RESPONSE.
           STOP RUN.
```

---

## 🧱 Filosofia  
> **Sentimentos são dados.**  
Mesmo caóticos, podem ser organizados, analisados e tratados com compaixão estruturada.

---

## 🌱 Roadmap  
- [ ] UI simples em HTML  
- [ ] Versão Python real  
- [ ] Interpreter emocional  
- [ ] Testes unitários  
- [ ] Módulos emocionais avançados  

---

## 📜 Licença  
MIT License  
