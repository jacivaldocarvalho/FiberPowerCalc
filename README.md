# 📡 FiberPowerCalc – Simulador de Orçamento de Potência Óptica

#### **Autor:** Jacivaldo Carvalho
#### **Data:** 13 de maio de 2025
#### **Versão:** v1.0.0 "init-dev"
---

## 🔍 Visão Geral

**FiberPowerCalc** é um aplicativo web projetado para **técnicos, engenheiros e instaladores de redes ópticas** que necessitam calcular o **orçamento de potência óptica** em enlaces de fibra. A plataforma permite simular diferentes cenários de instalação e verificar se o sinal final atende aos requisitos mínimos de sensibilidade do receptor.


## 🎯 Objetivo

Oferecer uma ferramenta intuitiva e técnica que:

* Permite entrada de parâmetros reais de um enlace óptico (tipo de fibra, conectores, emendas, splitters, distância, etc.);
* Calcula automaticamente perdas e potência final do sinal;
* Indica se o enlace está aprovado ou reprovado conforme os critérios de projeto.


## ⚙️ Funcionalidades Principais

* Simulação completa do **orçamento de potência óptica**;
* Validação técnica de enlace: status "Aprovado" ou "Reprovado";
* Geração de relatório técnico em **PDF**;
* Visualização gráfica da degradação do sinal;
* Inclusão de **cenários práticos reais**;
* Seleção do **tipo de rede óptica** (P2P, GPON, FTTH, Backbone, DWDM etc.);
* Interface moderna, responsiva e funcional.


## 🧮 Fórmula Base

```txt
Potência_final = Potência_emissor - (Σ perdas + margem de segurança)
```

### Fontes de Perda Consideradas:

| Item         | Valor Típico                    |
| ------------ | ------------------------------- |
| Fibra óptica | 0.35 dB/km (monomodo)           |
| Conectores   | 0.2 dB por conector             |
| Emendas      | 0.1 dB por fusão                |
| Splitters    | Ex: 1:2 ≈ 3.5 dB, 1:8 ≈ 10.5 dB |
| Margem       | Padrão de 3 dB (ajustável)      |


## 📝 Campos do Formulário

1. Tipo de fibra (monomodo / multimodo)
2. Distância do enlace (km)
3. Quantidade de conectores
4. Quantidade de emendas
5. Splitters e divisões (ex: 1:4, 1:8)
6. Potência do transmissor (dBm)
7. Sensibilidade mínima do receptor (dBm)
8. Margem de segurança (default: 3 dB)


## 🖥️ Tecnologias Utilizadas

| Camada          | Tecnologias                          |
| --------------- | ------------------------------------ |
| **Frontend**    | React + Vite                         |
| **Estilização** | Tailwind CSS                         |
| **Validação**   | React Hook Form + Yup                |
| **Gráficos**    | Recharts     |
| **Exportação**  | jsPDF (geração de relatório técnico) |
| **Hospedagem**  | Vercel                               |


## 📊 Resultados Gerados

* Tabela com perdas detalhadas por componente
* Potência final estimada (em dBm)
* Status do link: ✅ Aprovado ou ❌ Reprovado
* Gráfico da degradação do sinal ao longo do caminho
* Relatório em PDF técnico com todos os dados inseridos e cálculo detalhado


## 📸 Interface

* Layout técnico e funcional
* Design limpo e responsivo (cinza, azul e branco)
* Feedback visual direto sobre viabilidade do enlace


## 🧪 Casos de Teste Reais

### ✅ Cenário 1: Link Aprovado

Potência final: **-10.85 dBm** → ✅ Link aprovado

### ❌ Cenário 2: Link Reprovado

Potência final: **-25.8 dBm** → ❌ Link reprovado


## 🔧 Equipamentos Reais Referenciados

Inclui OLTs Huawei e FiberHome, ONTs Huawei/ZTE, fibras G.652D, splitters Furukawa/Intelbras, conectores SC/APC e SC/UPC, fusões com Fujikura, entre outros.


## 🌐 Tipos de Rede Suportados

* **Ponto a Ponto (P2P)**
* **GPON / FTTH**
* **FTTB / FTTC**
* **Backbone óptico**
* **DWDM (Dense Wavelength Division Multiplexing)**


## 🌈 Suporte a Cenários Avançados: DWDM

Simulação com canais de alta capacidade, MUX/DEMUX, EDFA e fibras G.652D/G.655.
Inclui ganho de amplificadores e perdas associadas a dispositivos passivos.


## 💡 Possibilidades de Expansão

* Multi-trecho com ganhos e perdas acumuladas
* Exportação para Excel
* Banco de dados com componentes reais
* Integração com ferramentas de gestão e mapeamento


## 📬 Contato

Jacivaldo Carvalho
🔗 \[[meu site](https://jacivaldocarvalho.vercel.app/)]


## 📄 Licença

Este projeto está licenciado sob os termos da **GNU General Public License v3.0**.

Você é livre para usar, estudar, modificar e distribuir este software, desde que preserve a mesma licença em qualquer redistribuição.

> Para mais informações, consulte o texto completo da licença em:
> [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html)

