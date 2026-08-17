# projeto-pratico
Este é o repositório da A1/1 de gerenciamento de configuração.


# Feature Boas vindas
Será criado um arquivo index.html que conterá uma pagina de boas vindas.


# Versionamento Semântico

O **Versionamento Semântico** é um padrão formal utilizado na engenharia de software para comunicar de forma clara o impacto de alterações entre diferentes lançamentos de um sistema ou biblioteca. Ele estabelece previsibilidade sobre compatibilidade e estabilidade de contratos de API.

O esquema segue o formato fundamental:

> **`MAJOR.MINOR.PATCH`** (exemplo: `1.4.2`)

---

## Estrutura e Regras de Incremento

| Segmento | Nome | Descrição | Quando Incrementar | Exemplo |
| :--- | :--- | :--- | :--- | :--- |
| **MAJOR** | Versão Principal | Mudanças incompatíveis na API pública (*Breaking Changes*). | Alteração ou remoção de endpoints, quebra de contratos de métodos existentes ou requisitos que exigem refatoração do consumidor. | `1.4.2` $\rightarrow$ `2.0.0` |
| **MINOR** | Versão Secundária | Adição de novas funcionalidades mantendo a retrocompatibilidade. | Inclusão de novas rotas, novos recursos, parâmetros opcionais ou marcação de APIs existentes como obsoletas (*deprecated*). | `1.4.2` $\rightarrow$ `1.5.0` |
| **PATCH** | Correção de Falhas | Correções de bugs mantendo a retrocompatibilidade. | Resolução de bugs internos, melhorias de desempenho e correções de segurança sem alteração de comportamento esperado da API. | `1.4.2` $\rightarrow$ `1.4.3` |

---

## Regras de Funcionamento

* **Reset de casas à direita:**
  * Incrementar **MAJOR** zera as posições `MINOR` e `PATCH` (`1.8.4` $\rightarrow$ `2.0.0`).
  * Incrementar **MINOR** zera a posição `PATCH` (`1.8.4` $\rightarrow$ `1.9.0`).
* **Fase inicial de desenvolvimento (`0.y.z`):** Versões no formato `0.x.x` indicam instabilidade. Alterações incompatíveis podem ocorrer a qualquer momento antes da versão `1.0.0`.
* **Sufixos opcionais:**
  * **Pré-lançamento:** Marcado por hífen (ex: `1.0.0-alpha.1`, `2.0.0-rc.3`).
  * **Build Metadata:** Marcado por sinal de adição (ex: `1.0.0+20260817.exp`).