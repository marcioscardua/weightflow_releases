# WeightFlow · Downloads (`weightflow_releases`)

Repositório **público** só de Releases: instaladores do WeightFlow desktop, `latest.json` e `SHA256SUMS`,
uma Release por versão `vX.Y.Z`. Nenhum código vive aqui — o desktop é desenvolvido em repositório
privado e o seu CI publica aqui a cada tag (ADR-019).

## Baixar

Abra [Releases](../../releases): a versão mais nova fica em destaque. Arquivos por versão:

| Arquivo | O que é |
|---|---|
| `WeightFlow_X.Y.Z_x64-setup.exe` | Instalador Windows padrão (baixa o WebView2 se faltar) |
| `WeightFlow_X.Y.Z_x64-setup-offline.exe` | Instalador Windows com WebView2 embutido — para PC sem internet |
| `WeightFlow_X.Y.Z_x64_en-US.msi` | MSI para instalação por política/TI |
| `latest.json` | Manifesto lido pela página de download do site |
| `SHA256SUMS` | Somas SHA-256 de todos os arquivos da versão |

Conferir a integridade (PowerShell): `Get-FileHash .\WeightFlow_X.Y.Z_x64-setup.exe -Algorithm SHA256`
e comparar com a linha correspondente em `SHA256SUMS`.

URL estável de cada arquivo:
`https://github.com/marcioscardua/weightflow_releases/releases/download/vX.Y.Z/<arquivo>`.

## Requisitos

Windows 10 ou 11 de 64 bits. Ubuntu (`.deb`, AppImage, `.rpm`) e macOS entram na matriz quando
forem homologados.

## Suporte

Dúvidas e problemas de instalação: pelo canal de atendimento informado no site. Este repositório
não recebe issues de código.
