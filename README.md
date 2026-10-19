# Brisa — navegador Android simples, sem anúncios

Implementação original (não copia código, imagens ou marca do app que inspirou o projeto).

## Recursos
- Várias abas (com restauração da sessão)
- Favoritos e histórico (SQLite local)
- Modo escuro (segue o sistema, claro ou escuro) e páginas escurecidas
- Bloqueio de anúncios e rastreadores por lista de domínios (`app/src/main/assets/blocklist.txt`)
- Downloads via DownloadManager
- Barra de pesquisa/endereço com mecanismo de busca à escolha (DuckDuckGo por padrão)
- Sem SDKs de anúncio/analytics; só a permissão de internet (e gravação em Downloads até o Android 9)

## Como gerar o APK
**Android Studio:** abra a pasta, aguarde o sync e use *Build > Build APK(s)*.

**GitHub Actions:** envie a pasta para um repositório; o workflow `.github/workflows/build.yml`
gera o APK debug em *Actions > Artifacts*.

**Linha de comando (Gradle 8.9 + Android SDK 35 + JDK 17):** `gradle assembleDebug`

## Aviso
O código foi escrito e verificado estaticamente (XML, ids e recursos), mas **não foi compilado**
no ambiente onde foi criado (sem Android SDK). O primeiro build pode pedir pequenos ajustes;
se der erro, envie o log que eu corrijo.
