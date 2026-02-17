# Action Tracker (Android)

App Android simples para registrar ações e acompanhar andamento.

## Funcionalidades
- Adicionar uma nova ação.
- Ver lista de ações cadastradas.
- Marcar/desmarcar cada ação como concluída.

## Como executar localmente
1. Abra o projeto no Android Studio (Hedgehog ou mais recente).
2. Aguarde sincronização do Gradle.
3. Rode no emulador/dispositivo Android (minSdk 24).

## Publicar APK no GitHub
Este repositório possui workflow em `.github/workflows/android-apk.yml` (sem depender de arquivos binários versionados no repositório).

- **Manual:** na aba **Actions**, execute o workflow **Build and Publish APK**.
  - O APK será anexado como artifact do workflow.
- **Automático em release:** ao criar/push de uma tag `v*` (ex: `v1.0.0`):
  - O workflow compila `assembleRelease` usando Gradle instalado no runner (não usa `gradle-wrapper.jar`).
  - Faz upload do `app-release-unsigned.apk` como artifact.
  - Publica o APK nos assets da Release no GitHub.

## Estrutura principal
- `MainActivity.kt`: tela principal com campo de input, botão de adicionar e lista com checkbox.

## Criar Pull Request
Se você não estiver conseguindo abrir PR, siga o guia em [`CONTRIBUTING.md`](CONTRIBUTING.md).
