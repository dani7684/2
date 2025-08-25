# Sistema de Eventos (Console, Java)

Atende aos requisitos: OOP, console, categorias limitadas (enum), cadastro de usuário (nome, email, cidade), cadastro/consulta de eventos (nome, endereço, categoria, horário **início e fim**, descrição), confirmação/cancelamento de presença, ordenação por proximidade de horário, indicação de "ocorrendo agora" e "já ocorreu", **persistência em `events.data`** (carrega ao iniciar e salva a cada alteração).

## Requisitos
- Java 11+ (recomendado Java 17)
- Terminal/console

## Compilar e executar
No diretório onde está o arquivo `EventConsoleApp.java`:

```bash
javac EventConsoleApp.java
java EventConsoleApp
```

O arquivo `events.data` será criado/atualizado no mesmo diretório.

## Formato de data/hora
- Entrada: `dd/MM/yyyy HH:mm` (ex.: `25/08/2025 19:30`)
- O sistema solicita **início** e **fim** do evento para identificar se está ocorrendo agora.

## Categorias (pré-definidas)
- FESTA, ESPORTE, SHOW, TEATRO, CONFERENCIA, FEIRA, RELIGIOSO, OUTRO

## Persistência
- `events.data` é salvo com pipe `|` como delimitador. Campos de texto têm `|` substituído por `/`.
- Participantes são armazenados por **ID** de usuário dentro de cada evento.

## Dicas
- Para rodar no **Eclipse**: crie um projeto Java, adicione `EventConsoleApp.java` à pasta `src` (sem pacote) e execute como "Java Application".
- Para um repositório **GitHub**: crie um repo, adicione `EventConsoleApp.java` e `events.data` (opcional vazio). Faça `git add . && git commit -m "Sistema de eventos console" && git push`.

Boa prática: evoluir para um pacote `br.seuapelido.eventos` e separar classes em arquivos distintos.
