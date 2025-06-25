# 🧠 Guia Prático de Comandos Git

## 📦 INICIALIZAÇÃO E CONFIGURAÇÃO

| Comando           | O que faz                                         |
| ----------------- | ------------------------------------------------- |
| `git init`        | Inicia um novo repositório Git no diretório atual |
| `git clone <url>` | Clona um repositório remoto já existente          |

---

## 📄 STATUS E INFORMAÇÕES

| Comando                     | O que faz                                               |
| --------------------------- | ------------------------------------------------------- |
| `git status`                | Mostra os arquivos modificados, adicionados e pendentes |
| `git log`                   | Mostra o histórico de commits                           |
| `git log --oneline --graph` | Histórico compacto com estrutura visual de branches     |

---

## ✏️ TRABALHANDO COM ARQUIVOS

| Comando                          | O que faz                                                |
| -------------------------------- | -------------------------------------------------------- |
| `git add <arquivo>`              | Adiciona um arquivo específico para staging (pré-commit) |
| `git add .`                      | Adiciona **todos** os arquivos modificados               |
| `git restore <arquivo>`          | Restaura um arquivo para o último commit                 |
| `git restore --staged <arquivo>` | Remove um arquivo da área de staging                     |

---

## ✅ COMMIT

| Comando                     | O que faz                                                 |
| --------------------------- | --------------------------------------------------------- |
| `git commit -m "mensagem"`  | Faz um commit com mensagem descritiva                     |
| `git commit -am "mensagem"` | Adiciona **e** faz commit direto dos arquivos modificados |

---

## 🔁 SINCRONIZAÇÃO COM O REMOTO

| Comando         | O que faz                                                |
| --------------- | -------------------------------------------------------- |
| `git remote -v` | Mostra os repositórios remotos configurados              |
| `git push`      | Envia seus commits para o repositório remoto             |
| `git pull`      | Traz as alterações do repositório remoto para o local    |
| `git fetch`     | Busca atualizações do repositório remoto **sem mesclar** |

---

## 🌿 RAMIFICAÇÕES (BRANCHES)

| Comando                  | O que faz                         |
| ------------------------ | --------------------------------- |
| `git branch`             | Lista todas as branches locais    |
| `git branch <nome>`      | Cria uma nova branch              |
| `git checkout <nome>`    | Troca para uma branch existente   |
| `git switch <nome>`      | Alternativa moderna ao `checkout` |
| `git checkout -b <nome>` | Cria e muda para uma nova branch  |
| `git merge <branch>`     | Mescla outra branch à atual       |
| `git branch -d <branch>` | Deleta uma branch local           |

---

## ⚠️ DESFAZENDO

| Comando                    | O que faz                                             |
| -------------------------- | ----------------------------------------------------- |
| `git reset --soft HEAD~1`  | Remove o último commit, mantendo arquivos no staging  |
| `git reset --mixed HEAD~1` | Remove o commit e tira arquivos do staging            |
| `git reset --hard HEAD~1`  | ⚠️ Remove o commit e as alterações — **irreversível** |
| `git revert <hash>`        | Cria um novo commit que desfaz o commit indicado      |

---

## 💡 DICAS RÁPIDAS

* Sempre faça `git pull` antes de começar a trabalhar.
* Faça commits pequenos e frequentes.
* Use mensagens claras: `"fix: corrigido bug do botão salvar"` ou `"feat: tela de login criada"`.
