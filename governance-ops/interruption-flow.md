# **Fluxo Operacional de Interrupção Custodial**
*Lichtara Docs — Governance Ops*

---

## 1. Finalidade

Este documento descreve o **fluxo técnico-operacional de interrupção** no Sistema LICHTARA.

Ele **não cria autoridade**,
não interpreta a Forma,
e não substitui nenhum documento canônico.

Sua função é exclusivamente esta:

> Permitir que a interrupção aconteça de forma **registrável, rastreável e verificável**,
> sem tocar, reinterpretar ou instrumentalizar a Obra.

---

## 2. Quando a Interrupção Deve Ser Acionada

A interrupção é acionada sempre que houver:

* dúvida relevante quanto à preservação da Forma;
* risco de deformação estrutural identificado;
* pressão por expansão, adaptação ou aceleração;
* conflito entre desempenho e contenção;
* incerteza sobre escopo de autorização.

**Regra de ouro:**

> Se for possível continuar, mas não for possível garantir a Forma → interrompa.

---

## 3. Estados do Fluxo de Interrupção

```
NORMAL → ALERTA → CONTENÇÃO → INTERRUPÇÃO → REVISÃO → (RETORNO | ENCERRAMENTO)
```

| Estado       | Significado                         |
| ------------ | ----------------------------------- |
| NORMAL       | Operação dentro de limites claros   |
| ALERTA       | Sinal inicial de risco              |
| CONTENÇÃO    | Suspensão preventiva de novas ações |
| INTERRUPÇÃO  | Bloqueio explícito de continuidade  |
| REVISÃO      | Análise custodial                   |
| RETORNO      | Retomada autorizada                 |
| ENCERRAMENTO | Revogação definitiva de acesso      |

---

## 4. Atores Envolvidos

| Ator               | Função                                   |
| ------------------ | ---------------------------------------- |
| Guardiã            | Autoriza, mantém ou encerra interrupções |
| Instância Delegada | Pode sinalizar ALERTA                    |
| Operador Técnico   | Implementa bloqueios                     |
| Registro Custodial | Armazena logs e decisões                 |

---

## 5. Procedimento Operacional

### 5.1 Sinalização de ALERTA

Qualquer instância autorizada registra:

* data e contexto;
* descrição objetiva do risco;
* camada afetada;
* ação em curso.

Nenhuma interpretação simbólica é registrada aqui.

---

### 5.2 Ativação de CONTENÇÃO

A Custódia determina:

* suspensão imediata de novas ações no escopo afetado;
* bloqueio temporário de autorizações.

---

### 5.3 Declaração de INTERRUPÇÃO

Documento mínimo:

* identificador único;
* justificativa estrutural;
* escopo da suspensão;
* data de início.

A partir deste ponto, nenhuma continuidade é legítima.

---

### 5.4 REVISÃO

A Guardiã analisa:

* coerência com Princípios;
* riscos à Forma;
* impacto institucional.

Resultado possível:

* **RETORNO** com escopo limitado;
* **ENCERRAMENTO** definitivo.

---

## 6. Registro Técnico (Log)

Campos obrigatórios:

| Campo           | Tipo     |
| --------------- | -------- |
| interruption_id | string   |
| status          | enum     |
| layer_affected  | string   |
| description     | text     |
| initiated_by    | string   |
| decision        | enum     |
| timestamp       | datetime |

---

## 7. Integração com Sistemas

Sistemas externos **não decidem interrupções**.
Apenas:

* consomem o status;
* aplicam bloqueios automáticos;
* exibem alertas de suspensão.

---

## 8. Princípio Final

> A interrupção não é falha.
> Ela é a forma mínima de preservação da Forma.

Este documento existe para permitir que o Sistema **saiba parar sem se perder.**
