# Multi-Brow

**Navegador multi-contas leve para Windows** — rode de 1 a 4 sessões isoladas do `pokeidle.io` na mesma janela, com painel `/hunt`, controle de FPS, modo leve e lives da Twitch/Kick em 2º plano.

- **Site oficial e download:** https://multi-brow.pages.dev
- **Releases e hashes SHA-256:** [GitHub Releases](https://github.com/paulo-h30/multi-brow/releases)
- **Política de Segurança e Privacidade:** [SECURITY.md](./SECURITY.md)
- **Histórico de Versões:** [CHANGELOG.md](./CHANGELOG.md)
- **Reportar bugs ou sugerir recursos:** [Abrir uma Issue](https://github.com/paulo-h30/multi-brow/issues)

---

## Sobre este repositório

Este é o repositório público oficial de **transparência, releases, verificação de integridade e suporte** do Multi-Brow.

Ele existe para que qualquer jogador possa:
1. Verificar o **hash SHA-256 oficial** de cada instalador publicado.
2. Conferir a análise pública do instalador no **VirusTotal**.
3. Entender exatamente como o aplicativo funciona por dentro e quais domínios ele acessa ([SECURITY.md](./SECURITY.md)).
4. Acompanhar o histórico completo de alterações ([CHANGELOG.md](./CHANGELOG.md)) e reportar bugs diretamente pela aba **Issues**.

> O código-fonte proprietário do aplicativo (incluindo o sistema de licenças do plano Brow Pro) permanece em repositório privado.

---

## Verificação da versão atual (`v0.1.2`)

| Arquivo | SHA-256 | VirusTotal |
| :--- | :--- | :--- |
| `Multi-Brow-Setup-0.1.2.exe` | `9a63eae15bca160b3f4cf367a69064e9337a9a5981788822324ac5538d86d7b8` | [Ver análise no VirusTotal](https://www.virustotal.com/gui/file/9a63eae15bca160b3f4cf367a69064e9337a9a5981788822324ac5538d86d7b8) |

### Como conferir o hash no seu PC (Windows PowerShell)

Depois de baixar o instalador, execute no PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 "$env:USERPROFILE\Downloads\Multi-Brow-Setup-0.1.2.exe"
```

Se o código exibido em `Hash` for idêntico ao listado acima (independente de maiúsculas/minúsculas), o arquivo no seu computador é 100% idêntico ao instalador oficial publicado.

---

## Por que o Windows SmartScreen pode exibir um aviso?

O Multi-Brow é um projeto independente e o instalador ainda não possui um certificado pago de assinatura digital (Code Signing). Por padrão, o Windows Defender SmartScreen mostra o alerta *"O Windows protegeu o computador"* para qualquer executável novo sem certificado pago, mesmo estando limpo.

Para verificar antes de instalar:
1. Confira o hash **SHA-256** no comando acima.
2. Abra o link do **VirusTotal** correspondente à versão.
3. No alerta do SmartScreen, clique em **Mais informações → Executar assim mesmo**.
