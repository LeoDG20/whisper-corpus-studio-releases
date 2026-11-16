<p align="center">
  <img src="assets/banner.png" alt="Whisper Corpus Studio" width="100%">
</p>

<p align="center">
  <a href="https://github.com/LeoDG20/whisper-corpus-studio-releases/releases/latest"><img alt="Versão" src="https://img.shields.io/github/v/release/LeoDG20/whisper-corpus-studio-releases?label=vers%C3%A3o&color=3B82F6&style=flat-square"></a>
  <a href="https://github.com/LeoDG20/whisper-corpus-studio-releases/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/LeoDG20/whisper-corpus-studio-releases/total?label=downloads&color=3B82F6&style=flat-square"></a>
  <img alt="Windows 10 e 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-1f2937?style=flat-square">
  <img alt="Assinatura Ed25519" src="https://img.shields.io/badge/atualiza%C3%A7%C3%A3o-assinada%20Ed25519-1f2937?style=flat-square">
</p>

<p align="center">
  <a href="https://github.com/LeoDG20/whisper-corpus-studio-releases/releases/latest"><b>⬇&nbsp; Baixar a versão mais recente</b></a>
</p>

Programa para Windows de **curadoria de corpus de fala sussurrada**: segmentar, revisar e exportar um dataset alinhado por fonemas a partir de áudios brutos.

## Recursos

- **Linha do tempo única:** fonemas, silêncio, ruído e respiração no mesmo eixo, sem camadas paralelas para conciliar.
- **Auto-segmentar assistido:** sugere as fronteiras e permite desfazer tudo (Ctrl+Z), inclusive os recortes criados.
- **Revisão guiada:** fila de curadoria ordenada por risco, com evidência acústica por fronteira.
- **Dataset auditável:** o pacote exportado traz manifesto com hashes, contagem por classe e versão do extrator.
- **Redes e parâmetros assinados:** recebe a rede neural e os parâmetros calibrados como pacotes verificados.

## Instalação

1. Em [Releases](https://github.com/LeoDG20/whisper-corpus-studio-releases/releases/latest), baixe **`WhisperCorpusStudio-Setup-<versão>.exe`**.
2. Execute o instalador. Requer Windows 10 ou 11 (64 bits); não precisa de administrador.
3. Se aparecer *“O Windows protegeu o computador”*, clique em **Mais informações → Executar assim mesmo** (veja a pergunta abaixo).

## Atualização automática e segurança

O programa instalado verifica este repositório e se atualiza sozinho, baixando apenas o que mudou. Antes de aplicar qualquer arquivo ele confere a **assinatura Ed25519** contra a chave pública embutida nele; arquivo sem assinatura válida é recusado. A chave privada fica apenas com o autor e nunca é publicada.

| Canal | Tag | Conteúdo |
| --- | --- | --- |
| Programa | `vX.Y.Z` | Instalador, atualização completa e incremental, manifesto assinado |
| Rede neural | `model-vX.Y.Z` | *Model pack* treinado no WCS-Net Trainer |
| Parâmetros | `params-vX.Y.Z` | Parâmetros de segmentação calibrados com o Gold Set |

## Perguntas frequentes

<details>
<summary><b>Por que o Windows mostra um aviso ao instalar?</b></summary>

O instalador não usa certificado comercial de editor, então o SmartScreen avisa para qualquer programa novo. A autenticidade é garantida pela assinatura Ed25519 descrita acima. Clique em **Mais informações → Executar assim mesmo**.

</details>

<details>
<summary><b>Onde ficam meus áudios e anotações?</b></summary>

No seu computador, em `%LocalAppData%`, separados do programa. Atualizar ou reinstalar não apaga esses dados.

</details>

<details>
<summary><b>Como desinstalo?</b></summary>

Em **Configurações do Windows → Aplicativos → Aplicativos instalados**.

</details>

<details>
<summary><b>Para que servem os outros arquivos de cada release?</b></summary>

Só o instalador (`Setup.exe`) interessa a quem instala. `manifest.json`, `package.zip`, `patch.zip` e os arquivos `.sig` são usados pela atualização automática e pela verificação de assinatura.

</details>

## Programas da família

| Programa | Função | Download |
| --- | --- | --- |
| **Whisper Corpus Studio** | Curadoria do corpus: segmentar, revisar e exportar o dataset. | [Baixar](https://github.com/LeoDG20/whisper-corpus-studio-releases/releases/latest) |
| WCS-Net Trainer | Treino das redes neurais a partir do dataset exportado pelo WCS. | [Baixar](https://github.com/LeoDG20/wcs-net-trainer-releases/releases/latest) |
| WCS Gold Set | Concordância entre versões de segmentação (você, orientador, colegas). | [Baixar](https://github.com/LeoDG20/wcs-gold-set-releases/releases/latest) |

---

<sub>Repositório de distribuição: o código-fonte é privado. Dúvidas ou problemas: abra uma <a href="https://github.com/LeoDG20/whisper-corpus-studio-releases/issues">issue</a>.<br>
© 2026 Leo Gobbi · uso acadêmico (TCC/IC).</sub>
