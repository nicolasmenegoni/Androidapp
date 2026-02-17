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

### Opção 1: criar Release manualmente (recomendado)
1. Vá em **Actions** > **Build and Publish APK**.
2. Clique em **Run workflow**.
3. Preencha:
   - `release_tag` (ex: `v1.0.0`)
   - `release_name` (ex: `Action Tracker v1.0.0`)
4. Execute o workflow.
5. Ao final, o `.apk` estará nos **assets** da Release criada no GitHub.

### Opção 2: por tag git
- Faça push de uma tag `v*` (ex: `v1.0.1`).
- O workflow compila e publica automaticamente o APK na Release dessa tag.

## Estrutura principal
- `MainActivity.kt`: tela principal com campo de input, botão de adicionar e lista com checkbox.

## Criar Pull Request
Se você não estiver conseguindo abrir PR, siga o guia em [`CONTRIBUTING.md`](CONTRIBUTING.md).
