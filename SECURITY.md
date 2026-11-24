# Segurança e Privacidade — Multi-Brow

Este documento explica com transparência como o **Multi-Brow** funciona no seu computador, quais dados ficam armazenados localmente, quais domínios de rede o aplicativo acessa e o que ele **nunca** faz.

---

## 1. Arquitetura e Isolamento

O Multi-Brow é construído sobre **Electron (Chromium)** com configurações estritas de isolamento nas janelas:

- **`contextIsolation: true`** — páginas web nunca têm acesso ao ambiente interno do Electron.
- **`nodeIntegration: false`** — páginas web não podem executar comandos do sistema nem acessar o sistema de arquivos.
- **`sandbox: true`** — processos de renderização rodam em sandbox do Chromium.
- **Partições de sessão isoladas:** cada conta do jogo utiliza sua própria partição local (`persist:account-1` a `persist:account-4`). Cookies, localStorage e sessões de login ficam separados entre si e armazenados apenas no perfil local do usuário (`%APPDATA%\multi-brow`).
- **Lives em 2º plano isoladas:** os logins da Twitch e da Kick usam partições próprias (`persist:stream-twitch` e `persist:stream-kick`), totalmente separadas das sessões do jogo.

---

## 2. O que o Multi-Brow NUNCA faz

- **Não lê nem envia arquivos pessoais** do seu computador (documentos, fotos, cookies de outros navegadores como Chrome/Edge/Firefox).
- **Não captura senhas nem faz keylogging.** Todos os logins (PokeIdle, Google, Discord, Twitch, Kick) acontecem diretamente nos sites oficiais carregados dentro das views do Chromium.
- **Não injeta código malicioso nem altera a memória** de outros programas do sistema.
- **Não executa mineração, proxy oculto nem processos escondidos** após o fechamento do aplicativo.

---

## 3. Lista transparente de domínios acessados

O aplicativo realiza conexões de rede apenas para os seguintes destinos:

| Domínio | Finalidade |
| :--- | :--- |
| `pokeidle.io` | Carregamento do jogo nas abas de conta. |
| `idlehub.io` | Janela opcional de voto (somente quando aberta pelo usuário). |
| `multi-brow.pages.dev` | Validação de licença (`Brow Free` / `Trial` / `Pro`), páginas de ajuda e changelog. |
| `pub-087760bbe10846f2b254398ab8940e20.r2.dev` | Verificação e download de atualizações oficiais (`latest.yml`, `changelog.json` e instalador NSIS). |
| `twitch.tv` / `kick.com` | Somente quando o usuário abre a janela de **Lives em 2º plano** e adiciona um canal. |

---

## 4. Verificação de integridade (SHA-256 e VirusTotal)

Todas as versões oficiais são publicadas com o hash **SHA-256** correspondente na página de [Releases](https://github.com/paulo-h30/multi-brow/releases).

Antes de executar o instalador, você pode conferir o hash localmente com:

```powershell
Get-FileHash -Algorithm SHA256 .\Multi-Brow-Setup-0.1.2.exe
```

E consultar a análise independente no VirusTotal pelo link `https://www.virustotal.com/gui/file/<SHA256>`.

---

## 5. Reportando problemas de segurança

Se você encontrar qualquer comportamento inesperado ou possível vulnerabilidade, abra uma Issue em [github.com/paulo-h30/multi-brow/issues](https://github.com/paulo-h30/multi-brow/issues) ou entre em contato pelos canais oficiais no site [multi-brow.pages.dev](https://multi-brow.pages.dev).
