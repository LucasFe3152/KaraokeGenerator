# YouTube Local Karaoke 🎤

Uma extensão de navegador open-source que transforma vídeos do YouTube em um karaokê em tempo real, rodando 100% no lado do cliente.

A extensão intercepta o áudio nativo do navegador, aplica processamento digital de sinais (DSP) localmente para remover os vocais da faixa e sincroniza o vídeo e as legendas originais do YouTube para compensar a latência do processamento.

## Funcionalidades

* **Remoção de Vocal em Tempo Real:** Utiliza a Web Audio API e AudioWorklets para processar o áudio isolando/atenuando a voz sem precisar baixar a música.
* **Zero Servidores Externos:** Todo o processamento matemático (via WebAssembly) acontece localmente no hardware do usuário.
* **Sincronização Automática:** Compensa a latência do DSP (~200ms) introduzindo um atraso milimétrico na tag `<video>` e na renderização das legendas nativas (DOM).
* **Legal e Seguro:** Não hospeda, não baixa e não distribui arquivos protegidos por direitos autorais.

## Tecnologias Utilizadas

* **JavaScript (ES6+)** para manipulação do DOM e injeção de scripts.
* **Web Audio API** para roteamento do fluxo de áudio interceptado.
* **AudioWorklet + WebAssembly (Wasm)** para processamento de sinais de baixa latência e alta performance fora da thread principal.

## Como Instalar (Modo Desenvolvedor)

1. Faça o download deste repositório em formato `.zip` e extraia os arquivos, ou clone via git
2. Ative o modo desenvolvedor na aba de extensões no seu navegador
3. Carregue o código da extensão
