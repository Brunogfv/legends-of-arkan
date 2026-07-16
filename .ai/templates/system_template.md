# Template de Sistema — Legends of Arkan

Use este template para documentar um novo sistema do jogo.
Sistemas são módulos independentes com responsabilidades bem definidas.

---

## Metadados

| Campo            | Valor          |
|------------------|----------------|
| **ID**           | SYS-[numero]   |
| **Nome**         |                |
| **Versão**       | 0.1.0          |
| **Criado em**    |                |
| **Autor**        | Arquiteto      |
| **Status**       | Esboço | Em Desenvolvimento | Estável | Depreciado |

---

## Visão Geral

[Descrição do propósito e responsabilidade do sistema]

---

## Dependências

### Este sistema depende de:
- [sistema] — [natureza da dependência]

### Sistemas que dependem deste:
- [sistema] — [natureza da dependência]

---

## Arquitetura

### Estrutura de Arquivos
```
game/systems/[nome]/
├── [nome].gd          # Classe principal
├── [nome].tscn        # Cena principal (se aplicável)
└── componentes/       # Subcomponentes
```

### Classes
| Classe      | Propósito                          | Herda de  |
|-------------|------------------------------------|-----------|
|             |                                    |           |

### Interfaces (Signals / Métodos Públicos)
```gdscript
signal [nome]([parametros])
func [nome]([parametros]) -> [retorno]
```

---

## Configuração

### Resources
| Resource    | Propriedades                     |
|-------------|----------------------------------|
|             |                                  |

### Export Variables
| Variável    | Tipo   | Padrão | Descrição       |
|-------------|--------|--------|-----------------|
|             |        |        |                 |

---

## Fluxo de Execução

```
[diagrama textual ou descrição do fluxo principal]
```

---

## Estados

| Estado      | Descrição                        | Transições           |
|-------------|----------------------------------|----------------------|
|             |                                  |                      |

---

## Tratamento de Erros

[Como o sistema lida com falhas, entradas inválidas, etc.]

---

## Testes

### Testes Unitários
- `tests/test_[sistema].gd` — [cobertura]

### Cenários de Teste
- [ ] [CT001]

---

## Histórico de Alterações

| Versão | Data       | Descrição | Autor |
|--------|------------|-----------|-------|
| 0.1.0  |            | Criação   |       |
