# Handoff — Sessão de estudo e Med Nykuto Core

Data: 2026-06-28
Repositório: drsoliveirasantos-lab/med-nykuto-core

## Objetivo deste arquivo

Guardar o essencial desta conversa para permitir sair da conversa atual e continuar os estudos ou o desenvolvimento do Med Nykuto em outra conversa.

Este arquivo NÃO é a transcrição completa palavra por palavra. É um resumo operacional: o que foi feito, como continuar, quais métodos foram definidos e quais pontos de estudo ficaram ativos.

---

# 1. Projeto Med Nykuto Core

Foi criado um ZIP inicial chamado:

- `MED_NYKUTO_CORE_v3_VOLUME_1.zip`

Esse ZIP foi gerado na conversa e contém a estrutura inicial do Core v3 Volume 1, com arquivos Markdown para metodologia, Exam Engine, Professor Engine, Medical Algorithms e templates.

O repositório GitHub identificado para o Core é:

- `drsoliveirasantos-lab/med-nykuto-core`

## Decisão de arquitetura

Foi decidido usar um repositório separado para o Core:

- `med-nykuto-core` = cérebro/metodologia/documentação.
- `med-nykuto` = site principal.
- Futuramente, pode existir `med-nykuto-question-bank` para bancos validados.

Motivo: evitar misturar site, código, prompts, bancos de questões e metodologia pedagógica no mesmo lugar.

---

# 2. Regras pedagógicas do Med Nykuto

## Regra central

O aluno deve responder antes de receber a correção.

## Formato preferido

1. Caso clínico curto.
2. Pergunta.
3. Alternativas A–D.
4. Aluno responde.
5. Correção imediata.
6. Justificativa da correta.
7. Justificativa das incorretas.
8. Ponto-chave de exame.
9. Próxima pergunta.

## Regras de qualidade

- Conteúdo médico final em espanhol médico claro.
- Casos clínicos com história realista.
- Distratores homogêneos.
- Evitar perguntas repetidas para preencher quantidade.
- Trabalhar módulo por módulo.
- Sempre identificar pontos fracos do aluno.
- Aumentar dificuldade progressivamente.

---

# 3. Professor Engine — Professora de Fisiologia

A professora explicou que a prova final será interpretativa, baseada em casos clínicos.

## Características da prova

- Fórmulas estarão disponíveis.
- Valores de referência laboratoriais virão junto.
- O índice reticulocitário é exceção: pode não vir com referência.
- Perguntas serão principalmente interpretativas, não diretas.
- Respostas escritas devem ser curtas: 2 a 5 palavras.
- Espera-se identificação de palavras-chave e justificativa.
- Não quer narração longa.

## Temas mais cobrados

1. Gasometria.
2. MIRO.
3. Compensação ácido-base.
4. Anion Gap.
5. Osmolaridade.
6. Potássio e potencial de ação.
7. Hemodinâmica.
8. Pressão arterial.
9. Gasto cardíaco.
10. Sistema simpático.

---

# 4. Algoritmos médicos estudados

## 4.1 MIRO

MIRO:

- M = Metabólico.
- I = Igual.
- R = Respiratório.
- O = Oposto.

Passos:

1. Ver pH.
   - pH < 7,35 = acidose.
   - pH > 7,45 = alcalose.

2. Ver HCO3.
   - Se HCO3 muda no mesmo sentido do pH, é metabólico.

3. Ver PCO2.
   - Se PCO2 muda no sentido oposto ao pH, é respiratório.

Exemplos:

- pH baixo + HCO3 baixo = acidose metabólica.
- pH alto + PCO2 baixo = alcalose respiratória.

## 4.2 Compensação da acidose metabólica

Fórmula usada pela professora:

```text
PCO2 esperado = HCO3 + 15 ± 2
```

Interpretação:

- Se PCO2 real está dentro do intervalo: compensação adequada.
- Se PCO2 real está fora: compensação inadequada ou transtorno misto.

Exemplo:

- HCO3 = 13.
- PCO2 esperado = 28 ± 2.
- Intervalo = 26–30.
- PCO2 real = 28 → compensação adequada.

## 4.3 Anion Gap

Fórmula:

```text
AG = Na - (Cl + HCO3)
```

Valor normal aproximado:

```text
8–12 mEq/L
```

Interpretação:

- AG normal: perda de bicarbonato.
  - Exemplo: diarreia.
  - Resposta de prova: acidose metabólica hiperclorêmica por perda de bicarbonato.

- AG elevado: produção/acúmulo de ácido.
  - Diabetes/cetonas → cetoacidose diabética.
  - Sepse/lactato → acidose láctica.
  - Insuficiência renal → ácidos urêmicos.

## 4.4 Osmolaridade

Fórmula:

```text
Osm = 2Na + glicose/18 + BUN/2,8
```

Normal:

```text
290–300 mOsm/L
```

Interpretação:

- Hipertônico: muito soluto ou perda de água.
- Hipotônico: excesso relativo de água.
- Isotônico: equilíbrio.

Ponto importante:

- Acidose não determina automaticamente osmolaridade.
- Quem determina é Na, glicose e BUN.

## 4.5 Potássio

Normal:

```text
K = 3,5–5,0 mEq/L
```

Hipopotassemia:

- K < 3,5.
- Causa fraqueza muscular.
- Mecanismo: hiperpolarização celular.
- Resposta de prova: `Hipopotasemia / hiperpolarización`.

## 4.6 Sódio

Normal:

```text
Na = 135–145 mEq/L
```

Hipernatremia:

- Na > 145.
- Aumenta osmolaridade.
- Pode indicar desidratação.

Hiponatremia:

- Na < 135.
- Pode causar edema celular/cerebral.

---

# 5. Hemodinâmica e vascular

## Fórmulas principais

```text
PA = GC × RVP
GC = VS × FC
```

## Hipovolemia/hemorragia/diarreia

Mecanismo:

1. Perda de volume.
2. Queda da PA.
3. Ativação simpática.
4. Aumento da FC.
5. Vasoconstrição periférica.
6. Tentativa de manter PA.

Resposta curta de prova:

- `Activación simpática`.
- `Aumento de FC y vasoconstricción`.

## Poiseuille

```text
R ∝ 1/r^4
```

Regras:

- raio ×2 → resistência ÷16.
- raio ÷2 → resistência ×16.

Fatores da resistência:

- raio: mais importante.
- viscosidade.
- comprimento do vaso.

## Velocidade e área transversal

```text
v = Q/A
```

- Maior velocidade: aorta.
- Maior pressão: aorta.
- Maior resistência: arteríolas.
- Maior área transversal: capilares.
- Menor velocidade: capilares.
- Maior volume armazenado: veias.

---

# 6. Renal — pontos revisados

Foram feitos blocos extensos sobre fisiologia renal.

## Pontos fortes do aluno

- SRAA.
- ADH.
- AINEs e prostaglandinas.
- Obstrução urinária.
- Túbulo proximal.
- Alça de Henle.

## Ponto fraco detectado

- Células intercaladas tipo A vs tipo B em ácido-base.

Regra:

| Situação | Célula | Ação |
|---|---|---|
| Acidosis | Tipo A | secreta H+, reabsorbe HCO3 |
| Alcalosis | Tipo B | secreta HCO3 |

Mnemônico:

- A = Acidosis = Tipo A.
- B = Básico/alcalosis = Tipo B.

---

# 7. Cardiovascular — arquivos enviados

O usuário enviou PDFs relacionados a:

- Fluxo sanguíneo.
- Sistema de condução.
- Coração e ciclo cardíaco.
- ECG.
- Sistema cardiovascular.
- Sangue.
- Hemostasia.

Foram iniciados casos sobre:

- nodo sinusal;
- nodo AV;
- Purkinje;
- ECG e direção do vetor;
- fluxo sanguíneo;
- Poiseuille;
- área transversal;
- pressão arterial;
- resistência vascular.

## Sistema de condução

Frequências úteis:

- Nodo sinusal: 60–100 bpm.
- Nodo AV: 40–60 bpm.
- Purkinje: 15–40 bpm.

Regra ECG:

- vetor indo em direção ao eletrodo positivo → onda positiva.
- vetor se afastando do eletrodo positivo → onda negativa.

---

# 8. Estado dos estudos antes de sair da conversa

## Prova amanhã

O plano recomendado foi estudar por blocos:

1. Gasometria + ácido-base.
2. Osmolaridade.
3. Potássio e potencial de ação.
4. Hemodinâmica.
5. Casos integrados estilo prova.

## Melhor formato para continuar

Na próxima conversa, pedir:

```text
Leia o handoff do GitHub e continue meu treino para a prova de Fisiologia usando o estilo da Professora de Fisiologia. Faça um caso clínico por vez, com respostas curtas e correção imediata.
```

## Próximo bloco sugerido

Continuar com vascular/hemodinâmica:

- pressão arterial;
- fluxo;
- resistência;
- retorno venoso;
- simpático;
- pré-carga;
- pós-carga;
- débito cardíaco;
- casos integrados com gasometria e eletrólitos.

---

# 9. Prompts úteis para continuar

## Prompt para continuar estudo

```text
Quero continuar a revisão de Fisiologia para a prova de amanhã.
Use o estilo da professora: casos clínicos interpretativos, respostas curtas de 2–5 palavras, MIRO, compensação, Anion Gap, osmolaridade, potássio e hemodinâmica.
Faça uma pergunta por vez e espere minha resposta.
Depois corrija curto, explique o mecanismo e siga para a próxima.
```

## Prompt para continuar Med Nykuto Core

```text
Use o repositório drsoliveirasantos-lab/med-nykuto-core como base.
Continue desenvolvendo o Med Nykuto Core v3 seguindo a Constituição, Exam Engine, Professor Engine e AI Engine já definidos.
```

---

# 10. Respostas modelo que o aluno deve memorizar

- Acidosis metabólica compensada.
- Compensación respiratoria adecuada.
- Acidosis metabólica hiperclorémica.
- Pérdida de bicarbonato por diarrea.
- Anion gap elevado.
- Cetoacidosis diabética.
- Acidosis láctica por sepsis.
- Hipopotasemia e hiperpolarización.
- Activación simpática.
- Aumento de frecuencia cardíaca y vasoconstricción.
- Plasma hipertónico por hipernatremia/deshidratación.

---

# 11. O que ainda falta salvar no futuro

Este handoff guarda o essencial, mas não contém todas as perguntas palavra por palavra.

Próximos passos para o repositório:

1. Subir o conteúdo completo do ZIP Volume 1 como arquivos separados.
2. Criar `study-sessions/` com sessões futuras.
3. Criar `question-banks/physiology/` com casos validados.
4. Criar `professor-engine/fisiologia.md` completo.
5. Criar `medical-engine/gasometria/` completo.
6. Criar `medical-engine/hemodinamica/` completo.
