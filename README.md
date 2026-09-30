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
| `WeightFlow_X.Y.Z_x64_pt-BR.msi` | MSI para instalação por política/TI |
| `WeightFlow_X.Y.Z_amd64.deb` | Pacote para Ubuntu e Debian (`sudo apt install ./arquivo.deb`) |
| `WeightFlow_X.Y.Z_amd64.AppImage` | Linux, qualquer distribuição: `chmod +x` e abrir (precisa do WebKitGTK 4.1) |
| `WeightFlow-X.Y.Z-1.x86_64.rpm` | Pacote para Fedora e RHEL (`sudo dnf install ./arquivo.rpm`) |
| `WeightFlow_X.Y.Z_universal.dmg` | macOS, um arquivo só para Mac com Apple Silicon ou Intel: abra e arraste o WeightFlow para Aplicativos (nas versões que trazem o `.dmg`) |
| `latest.json` | Manifesto da versão: a página de download do site é montada a partir dele |
| `SHA256SUMS` | Somas SHA-256 de todos os arquivos da versão |

Conferir a integridade — Windows (PowerShell): `Get-FileHash .\WeightFlow_X.Y.Z_x64-setup.exe -Algorithm SHA256`
e comparar com a linha correspondente em `SHA256SUMS`; Linux: `sha256sum -c SHA256SUMS --ignore-missing`
na pasta do download; macOS (Terminal): `shasum -a 256 WeightFlow_X.Y.Z_universal.dmg` e comparar com a
linha correspondente em `SHA256SUMS`.

URL estável de cada arquivo:
`https://github.com/marcioscardua/weightflow_releases/releases/download/vX.Y.Z/<arquivo>`.

## Requisitos

Windows 10 ou 11 de 64 bits (plataforma principal). Linux de 64 bits com WebKitGTK 4.1 — Ubuntu 22.04,
Debian 12, Fedora 40 ou mais novos (plataforma secundária); para a porta serial, o usuário precisa estar
no grupo `dialout`. macOS 11 ou mais novo, em Mac com Apple Silicon ou Intel (plataforma secundária, com
homologação depois do Windows).

Se, na primeira abertura, o macOS avisar que não pôde verificar o app ou o desenvolvedor: feche o aviso,
abra Ajustes do Sistema → Privacidade e Segurança e, em Segurança, clique em “Abrir Mesmo Assim”
(até o macOS 12: Preferências do Sistema → Segurança e Privacidade → Geral).

## Suporte

Dúvidas e problemas de instalação: pelo canal de atendimento informado no site. Este repositório
não recebe issues de código.
