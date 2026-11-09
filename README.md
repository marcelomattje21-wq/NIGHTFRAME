# NIGHTFRAME Studio

Projeto desktop para criação de vídeos Lo-Fi a partir de ilustrações estáticas.

## Versão em desenvolvimento: V38

A V38 acrescenta:
- Segmentação semântica local com Transformers.js + SegFormer-B0 quantizado em CPU.
- Ferramenta IA Loop com seleção de regiões, refinamento por pincel/borracha e animação periódica.
- Exportação de loops MP4 em 1080p pelo FFmpeg local.
- Atualizações automáticas via electron-updater e GitHub Releases (instalador NSIS).

## Estado do repositório

O repositório foi inicializado. O pacote-fonte completo da V38 ainda precisa ser enviado para a raiz deste repositório antes de gerar a primeira release instalável. O arquivo-fonte contém o projeto Electron, o motor FFmpeg, os testes e o workflow de publicação para Windows.

## Requisitos de build

- Windows 10/11 x64
- Node.js 22+
- PowerShell
- Conexão à internet na preparação inicial para baixar FFmpeg e dependências npm

Depois de enviar os arquivos da V38, execute `BUILD_NIGHTFRAME_DESKTOP.bat` para gerar o instalador NSIS. A primeira instalação da V38 é manual; as versões posteriores podem ser atualizadas pelo próprio aplicativo.

## IA local

Modelo: [Xenova/segformer-b0-finetuned-ade-512-512](https://huggingface.co/Xenova/segformer-b0-finetuned-ade-512-512). O modelo é baixado no primeiro uso e executado localmente. Não há cobrança por créditos de geração; a análise de imagens não é enviada para uma API de inferência.
